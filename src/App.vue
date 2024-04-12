<script setup lang="ts">
import { onErrorCaptured } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'
import { ref } from 'vue'
const menuIsOpen = ref(false)

onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})
</script>

<template>
  <header class="m-2">
    <button
      aria-controls="mainNav"
      aria-expanded="true"
      class="rounded-full border-2 border-indigo-800 bg-indigo-300 px-2 text-indigo-800 hover:text-indigo-100 hover:bg-indigo-500 transition-colors duration-300"
      @pointerdown="menuIsOpen = !menuIsOpen"
      >
      menu
    </button>
<!-- nav#mainNav>ul>li*3>a[href="#"]{item $} -->
<Transition
  class="transition-transform duration-300"
  enter-from-class="-translate-x-full"
  enter-to-class="translate-x-0"
  leave-active-class="-translate-x-full"
>
    <nav id="mainNav" v-show="menuIsOpen">
      <ul class="*:text-indigo-500">
        <li>
          <RouterLink to="/" class="hover:underline">Accueil </RouterLink>
        </li>
        <li>
          <RouterLink to="/accordeon" class="hover:underline"> Accordeon </RouterLink>
        </li>
        <li>
          <RouterLink to="/boucle" class="hover:underline"> Boucle sur des données </RouterLink>
        </li>
      </ul>
    </nav>
  </Transition>
  </header>
  <RouterView v-slot="{ Component }">
    <Suspense>
      <component :is="Component" />
    </Suspense>
  </RouterView>
</template>
