<script setup>
import { ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'
import NavItem from './NavItem.vue'

const navItems = [
  { name: 'timeline', icon: ClockIcon },
  { name: 'activities', icon: ListBulletIcon },
  { name: 'progress', icon: ChartBarIcon }
]
</script>

<template>
  <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <NavItem v-for="(item, index) in navItems" :key="index" :href="`#${item.name}`">
        <component :is="item.icon" class="h-6 w-6"></component>{{ item.name }}
      </NavItem>
    </ul>
  </nav>
</template>
