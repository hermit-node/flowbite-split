<script lang="ts" setup>
import * as IconsVue from '@tabler/icons-vue';

const c0 = "#373a48"
const c1 = "#325dff"
const c2 = "#c20f8f"
const c3 = "#0ed018"
const c4 = "#ffb500"
const c5 = "#d132ff"
const c6 = "#22a18c"
</script>

<template>
  <button data-drawer-target="default-sidebar" data-drawer-toggle="default-sidebar" aria-controls="default-sidebar" type="button" class="inline-flex items-center p-2 mt-2 ml-3 text-sm text-gray-500 rounded-lg sm:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600">
    <span class="sr-only">Open sidebar</span>
    <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
      <path clip-rule="evenodd" fill-rule="evenodd" d="M2 4.75A.75.75 0 012.75 4h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 4.75zm0 10.5a.75.75 0 01.75-.75h7.5a.75.75 0 010 1.5h-7.5a.75.75 0 01-.75-.75zM2 10a.75.75 0 01.75-.75h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 10z"></path>
    </svg>
  </button>

  <aside id="default-sidebar" class="fixed top-0 left-0 z-40 w-64 h-screen transition-transform -translate-x-full sm:translate-x-0" aria-label="Sidenav">
    <div class="overflow-y-auto py-5 px-3 h-full bg-white border-r border-gray-200 dark:bg-gray-800 dark:border-gray-700">
      <ul class="space-y-2">
        <li>
          <router-link to="/" class="menu-item">
            <IconsVue.IconHome2 class="w-6 h-6 text-gray-400 transition duration-75" :color="c5" stroke="3"/>
            <span>Home</span>
          </router-link>
        </li>
        <li>
          <router-link to="/events" class="menu-item">
            <IconsVue.IconCalendar class="w-6 h-6 text-gray-400 transition duration-75" :color="c6" stroke="3"/>
            <span>Events (data attributes)</span>
          </router-link>
        </li>
        <li>
          <router-link to="/accordion" class="menu-item">
            <IconsVue.IconAccessPointOff class="w-6 h-6 text-gray-400 transition duration-75" :color="c3" stroke="3"/>
            <span>Accordion</span>
          </router-link>
        </li>
        <li>
          <router-link to="/carousel" class="menu-item">
            <IconsVue.IconCarouselVertical class="w-6 h-6 text-gray-400 transition duration-75" :color="c2" stroke="3"/>
            <span>Carousel</span>
          </router-link>
        </li>
        <li>
          <router-link to="/modal" class="menu-item">
            <IconsVue.IconToiletPaper class="w-6 h-6 text-gray-400 transition duration-75" :color="c4" stroke="3"/>
            <span>Modal</span>
          </router-link>
        </li>
        <li>
          <router-link to="/collapse" class="menu-item">
            <IconsVue.IconChartAreaLine class="w-6 h-6 text-gray-400 transition duration-75" :color="c1" stroke="3"/>
            <span>Collapse</span>
          </router-link>
        </li>
        <li>
          <router-link to="/dial" class="menu-item">
            <IconsVue.IconPhoneCall class="w-6 h-6 text-gray-400 transition duration-75" :color="c2" stroke="3"/>
            <span>Speed Dial</span>
          </router-link>
        </li>
        <li>
          <router-link to="/dismiss" class="menu-item">
            <IconsVue.IconDiaboloPlus class="w-6 h-6 text-gray-400 transition duration-75" :color="c6" stroke="3"/>
            <span>Dismiss</span>
          </router-link>
        </li>
        <li>
          <router-link to="/drawer" class="menu-item">
            <IconsVue.IconChartPieFilled class="w-6 h-6 text-gray-400 transition duration-75" :color="c0" stroke="3"/>
            <span>Drawer</span>
          </router-link>
        </li>
        <li>
          <router-link to="/dropdown" class="menu-item">
            <IconsVue.IconBorderBottomPlus class="w-6 h-6 text-gray-400 transition duration-75" :color="c2" stroke="3"/>
            <span>Dropdown</span>
          </router-link>
        </li>
        <li>
          <router-link to="/popover" class="menu-item">
            <IconsVue.IconEaseInOut class="w-6 h-6 text-gray-400 transition duration-75" :color="c4" stroke="3"/>
            <span>Popover</span>
          </router-link>
        </li>
        <li>
          <router-link to="/tabs" class="menu-item">
            <IconsVue.IconTableMinus class="w-6 h-6 text-gray-400 transition duration-75" :color="c5" stroke="3"/>
            <span>Tabs</span>
          </router-link>
        </li>
        <li>
          <router-link to="/tooltip" class="menu-item">
            <IconsVue.IconTooltip class="w-6 h-6 text-gray-400 transition duration-75" :color="c1" stroke="3"/>
            <span>Tooltip</span>
          </router-link>
        </li>
        <li>
          <router-link to="/input-counter" class="menu-item">
            <IconsVue.IconClockPlus class="w-6 h-6 text-gray-400 transition duration-75" :color="c2" stroke="3"/>
            <span>Input Counter</span>
          </router-link>
        </li>
      </ul>
    </div>
  </aside>

  <div class="flex items-center justify-center h-screen bg-gray-50">
    <div>
      <h1 class="mb-6 text-4xl">Flowbite + Vue 3 + Tailwind CSS Starter</h1>
      <router-view />
    </div>
  </div>
</template>

<style scoped>
.menu-item {
  @apply flex items-center p-2 text-base font-normal text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700;
}
.menu-item svg {
  @apply flex-shrink-0 w-6 h-6 text-gray-400 transition duration-75 group-hover:text-gray-900 dark:group-hover:text-white;
}
.menu-item span {
  @apply ml-3;
}
</style>
