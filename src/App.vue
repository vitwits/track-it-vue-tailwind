<script setup>
import { CheckCircleIcon } from '@heroicons/vue/24/solid'
import { ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'

const navItems = ['timeline', 'activities', 'progress']
</script>

<template>
  <header class="sticky top-0 z-20 flex items-center justify-between border-b bg-white p-3">
    <a href="#"><img src="./assets/logo.png" alt="Logo" class="h-9" /></a>
    <a href="#" class="text-sm">
      <div v-if="true" class="flex items-center gap-1">
        Day completed!
        <CheckCircleIcon class="h-7 text-green-500" />
      </div>
      <div v-else class="flex items-center gap-1">
        <div>Progress: <span class="font-mono">20%</span></div>
        <div class="h-3 w-3 rounded-full bg-red-500"></div>
      </div>
    </a>
  </header>
  <main class="flex flex-grow flex-col">
    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Modi voluptate quis aliquid nobis,
    quam optio? Veniam itaque delectus blanditiis tempora illo iusto commodi! Incidunt quod
    voluptatum unde doloribus laudantium nulla sint, excepturi recusandae eos cupiditate ducimus ut
    possimus debitis iusto placeat, facere, quia obcaecati vel illo! Quidem hic eveniet totam nihil
    rem cupiditate suscipit explicabo, consectetur itaque ipsam quisquam nulla saepe tempora,
    pariatur rerum ipsum. Dolores eaque distinctio accusantium? Ratione explicabo sequi sunt
    consectetur fugit doloribus aut rerum! At, alias ut! Mollitia id quis, autem, amet laborum velit
    quas ratione dolores obcaecati quisquam rerum quos eos reiciendis omnis itaque molestias ipsa,
    architecto suscipit libero aperiam tempore minus quo. Cum expedita perspiciatis vel amet
    possimus exerci sed totam
  </main>
  <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <li v-for="(page, key) in navItems" v-bind:key="key" class="flex-1">
        <a v-bind:href="`#${page}`" class="flex flex-col items-center p-2 text-xs capitalize">
          <ClockIcon v-if="page === 'timeline'" class="h-6 w-6" />
          <ListBulletIcon v-else-if="page === 'activities'" class="h-6 w-6" />
          <ChartBarIcon v-else class="h-6 w-6" /> {{ page }}
        </a>
      </li>
    </ul>
  </nav>
</template>
