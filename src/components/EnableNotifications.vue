<template>
  <!-- <div class="py-16">
    <Switch
      v-model="enabled"
      :class="enabled ? 'bg-teal-900' : 'bg-teal-700'"
      class="relative inline-flex flex-shrink-0 h-[38px] w-[74px] border-2 border-transparent rounded-full cursor-pointer transition-colors ease-in-out duration-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
    >
      <span class="sr-only">Use setting</span>
      <span
        aria-hidden="true"
        :class="enabled ? 'translate-x-9' : 'translate-x-0'"
        class="pointer-events-none inline-block h-[34px] w-[34px] rounded-full bg-white shadow-lg transform ring-0 transition ease-in-out duration-200"
      />
    </Switch>
  </div> -->

  <SwitchGroup>
    <div class="flex justify-between items-center max-w-sm mx-auto">
      <SwitchLabel class="mr-4">Switch (Toggle)</SwitchLabel>
      <Switch
        v-model="enabled"
        :class='enabled ? "bg-blue-600" : "bg-gray-200"'
        class="relative inline-flex items-center h-6 transition-colors rounded-full w-11 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
      >
        <span class="sr-only">Use setting</span>
        <span
          :class='enabled ? "translate-x-6" : "translate-x-1"'
          class="inline-block w-4 h-4 transition-transform transform bg-white rounded-full"
        />
      </Switch>
    </div>
  </SwitchGroup>
</template>

<script>
  import { getCurrentInstance, ref, onMounted, onUpdated, onUnmounted } from 'vue'
  import { Switch, SwitchGroup, SwitchLabel } from '@headlessui/vue'

  export default {
    components: { Switch, SwitchGroup, SwitchLabel },

    setup() {
      const enabled = ref(false)
      console.log("Switch (toggle) enabled = ", enabled.value)

      onMounted(() => {
        console.log('Switch mounted!')
      })
      onUpdated(() => {
        console.log('Switch updated!')
      })
      onUnmounted(() => {
        console.log('Switch unmounted!')
      })

      return { enabled }
    },
  }
</script>