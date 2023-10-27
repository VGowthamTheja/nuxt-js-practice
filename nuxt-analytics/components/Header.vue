<template>
  <header class="sticky top-0 z-20 border-b bg-background/80 backdrop-blur">
    <div class="container flex h-16 items-center justify-between">
      <div class="flex items-center gap-3">
        <img src="/icon.svg" alt="Logo" class="h-7 w-7 object-contain" />
        <NuxtLink to="/" class="text-2xl font-bold text-primary">Dashboard</NuxtLink>
      </div>

      <div class="flex items-center gap-5">
        <button @click="toggleMode" aria-label="Toggle color mode"
          class="flex h-9 w-9 shrink-0 items-center justify-center rounded-full border bg-background">
          <Icon v-if="mode === 'dark'" name="heroicons-sun" class="h-7 w-7 text-yellow-500" />
          <Icon v-if="mode === 'light'" name="heroicons-moon" class="h-7 w-7 text-purple-900 " />
        </button>

        <HMenu as="div" class="relative">
          <HMenuButton class="flex h-9 w-9 shrink-0 items-center justify-center rounded-full border bg-background">
            <img src="https://randomuser.me/api/portraits/med/men/75.jpg" alt="Profile"
              class="rounded-full object-cover" />
          </HMenuButton>
          <TransitionScale :scale="0.8" origin="top-right">
            <HMenuItems
              class="absolute right-0 z-10 mt-3 w-48 rounded-md border bg-background focus:outline-none focus-visible:ring-2 focus-visible:ring-ring">
              <div class="border-b px-3 py-1.5 text-sm">
                <p class="font-semibold pt-1">Hello Jhon!</p>
                <a href="mailto:jhondoe@test.com" class="leading-none text-muted-foreground">jhondoe@test.com</a>
              </div>
              <div class="p-1">
                <template v-for="(p, i) in profileMenuOptions" :key="i">
                  <HMenuItem v-if="!p.divider" v-slot="{ active }">
                    <button :class="[active && 'bg-muted']"
                      class="w-full text-left px-3 py-1.5 text-sm hover:bg-slate-200 dark:hover:text-black focus:outline-none focus-visible:ring-2 focus-visible:ring-ring rounded-md">
                      {{ p.title }}
                    </button>
                  </HMenuItem>
                  <hr v-if="p.divider" />
                </template>
              </div>
            </HMenuItems>
          </TransitionScale>
        </HMenu>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>
const mode = useColorMode();
const toggleMode = () => mode.value = mode.value === 'dark' ? 'light' : 'dark';
const profileMenuOptions = [
  { title: "Profile" },
  { title: "Billing" },
  { title: "Settings" },
  { title: "Team members" },
  { title: "Sales" },
  { divider: true },
  { title: "Logout" },
];
</script>

<style></style>

