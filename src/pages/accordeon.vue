<script setup lang="ts">
import { ref } from 'vue'
const sectionOpen = ref(0)
</script>
<template>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen =  sectionOpen === 1 ? 0:1">bouton 1</button>
        <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit libero saepe et ipsam atque magni placeat quibusdam doloremque asperiores, error modi doloribus mollitia inventore odio optio magnam praesentium ducimus eligendi.</p>
    </section>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen =  sectionOpen === 2 ? 0:2">bouton 2</button>
        <p v-show="sectionOpen === 2">Expedita laboriosam temporibus maiores quidem facere velit ea ut sed eius ipsum illum repudiandae aliquid magnam impedit distinctio suscipit quaerat voluptates quibusdam exercitationem voluptatum, ipsa eos minus commodi? Vitae, tenetur!</p>
    </section>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen =  sectionOpen === 3 ? 0:3">bouton 3</button>
        <p v-show="sectionOpen === 3">Deserunt, neque provident! Numquam, veniam blanditiis deleniti, eos soluta, delectus illo possimus nemo labore ratione id recusandae molestiae sit sed autem esse iste sequi praesentium? Atque amet ipsum accusamus quisquam?</p>
    </section>
</template>