<script setup lang="ts">
const pages: { title: string; path: string }[] = [
  {
    title: "Avatars",
    path: "/components/avatars",
  },
  {
    title: "Badges",
    path: "/components/badges",
  },
  {
    title: "Alerts",
    path: "/components/alerts",
  },
  {
    title: "Buttons",
    path: "/components/buttons",
  },
  {
    title: "Bottom Navigations",
    path: "/components/bottomnavigations",
  },
  {
    title: "Checkboxes",
    path: "/components/checkboxes"
  },
  // {
  //   title: 'Drawers',
  //   path: '/Components/drawers'
  // },
  {
    title: "Dropdowns",
    path: "/components/dropdowns",
  },
  {
    title: "File Inputs",
    path: "/components/fileinputs"
  },
  {
    title: "Links",
    path: "/components/links",
  },
  {
    title: "Modals",
    path: "/components/modals",
  },
  {
    title: "Menus",
    path: "/components/menus",
  },
  {
    title: "Navbars",
    path: "/components/navbars",
  },
  {
    title: "Paginations",
    path: "/components/paginations",
  },
  {
    title: "Radios",
    path: "/components/radios",
  },
  {
    title: "Range Sliders",
    path: "/components/rangesliders"
  },
  {
    title: "Tabs",
    path: "/components/tabs",
  },
];
</script>
<template>
  <section class="drawer lg:drawer-open">
    <input id="my-drawer" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content">
      <div class="navbar bg-base-100">
        <div class="flex-none">
          <label
            for="my-drawer"
            class="btn btn-square btn-ghost drawer-button lg:hidden"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              class="inline-block w-5 h-5 stroke-current"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </label>
        </div>
        <div class="flex-1">
          <NuxtLink to="/" class="btn btn-ghost text-xl"
            >Nirvana UI
            <span class="badge badge-primary text-xs">powered by daisyUI</span>
          </NuxtLink>
        </div>
      </div>
      <NuxtPage />
    </div>
    <div
      class="drawer-side z-40"
      style="scroll-behavior: smooth; scroll-padding-top: 5rem"
    >
      <label
        for="my-drawer"
        aria-label="close sidebar"
        class="drawer-overlay"
      ></label>
      <ul class="menu p-4 w-80 min-h-full bg-base-200 text-base-content">
        <div class="text-xl font-bold my-3">Components</div>
        <li v-for="page in pages" :key="page.path">
          <NuxtLink :to="page.path">{{ page.title }}</NuxtLink>
        </li>
      </ul>
    </div>
  </section>
</template>
