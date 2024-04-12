<script setup lang="ts">
import { ref } from 'vue'
const sectionOpen = ref(0)

</script>
<template>
    <div class="m-2 flex flex-col gap-2">
    <section>
        <button class="text-xl bg-indigo-500 px-3 py-1 rounded-md text-white hover:bg-indigo-400 transition-colors duration-300" @pointerdown="sectionOpen =  sectionOpen === 1 ? 0:1">bouton 1</button>
        <Transition
        class="transition-transform duration-300"
        enter-to-class="translate-x-0"
        leave-active-class="-translate-x-full"
        enter-from-class="-translate-x-full"
        >
        <p class="" v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit libero saepe et ipsam atque magni placeat quibusdam doloremque asperiores, error modi doloribus mollitia inventore odio optio magnam praesentium ducimus eligendi.</p>
        </Transition>
</section>
    <section>
        <button class="text-xl bg-indigo-500 px-3 py-1 rounded-md text-white hover:bg-indigo-400 transition-colors duration-300" @pointerdown="sectionOpen =  sectionOpen === 2 ? 0:2">bouton 2</button>
        <Transition
        class="transition-transform duration-300"
        enter-to-class="translate-x-0"
        leave-active-class="-translate-x-full"
        enter-from-class="-translate-x-full"
        >
        <p v-show="sectionOpen === 2">Expedita laboriosam temporibus maiores quidem facere velit ea ut sed eius ipsum illum repudiandae aliquid magnam impedit distinctio suscipit quaerat voluptates quibusdam exercitationem voluptatum, ipsa eos minus commodi? Vitae, tenetur!</p>
        </Transition>
    </section>
    <section>
        <button class="text-xl bg-indigo-500 px-3 py-1 rounded-md text-white hover:bg-indigo-400 transition-colors duration-300" @pointerdown="sectionOpen =  sectionOpen === 3 ? 0:3">bouton 3</button>
        <Transition
        class="transition-transform duration-300"
        enter-to-class="translate-x-0"
        leave-active-class="-translate-x-full"
        enter-from-class="-translate-x-full"
        >
        <p v-show="sectionOpen === 3">Deserunt, neque provident! Numquam, veniam blanditiis deleniti, eos soluta, delectus illo possimus nemo labore ratione id recusandae molestiae sit sed autem esse iste sequi praesentium? Atque amet ipsum accusamus quisquam?</p>
        </Transition>
    </section>
    </div>
</template>