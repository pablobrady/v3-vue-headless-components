<template>
  <Menu as="div">
    <MenuButton>
      <button class="w-full inline-flex justify-center items-center px-3 py-2 text-sm leading-4 font-medium shadow-sm text-white bg-green-500 hover:text-gray-700 hover:bg-yellow-300 focus:outline-none first:border-l-2 border-r-2 border-green-500">
        Dropdown Menu
        <ChevronDownIcon
          class="w-5 h-5 ml-2 -mr-1 text-violet-200 hover:text-violet-100"
          aria-hidden="true"
        />

      </button>
    </MenuButton>
    <MenuItems v-for="(item) in items" class="list-none bg-yellow-100 focus:outline-none">
      <MenuItem v-slot="{ active }">
        <a
          :class="[
            active
              ? 'bg-yellow-300'
              : 'bg-yellow-100',
          ]"

          class="block"
          href="#"
        >
          {{ item }}
        </a>
      </MenuItem>
    </MenuItems>
  </Menu>
</template>

<script>
  import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
  import { ChevronDownIcon } from '@heroicons/vue/solid'

  export default {
    components: {
      Menu,
      MenuButton,
      MenuItems,
      MenuItem,
      ChevronDownIcon,
    },
    data() {
      return {
        items: ['Feed the cat', 'Buy milk', 'Let the dog out']
      }
    },
  };
</script>