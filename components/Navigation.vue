<script setup>
import { ref } from 'vue'

const count = ref(0)
const isShown = ref(true)

function increment() {
  count.value += 2
}
</script>

<template>
  <div class="container" :class="{show:isShown}">
    <NuxtLink to="/"><div class="link">Home</div></NuxtLink>
    <NuxtLink to="/about"><div class="link">Identitas</div></NuxtLink>
    <NuxtLink to="/gallery"><div class="link">Galeri</div></NuxtLink>
    <NuxtLink to="/members"><div class="link">Anggota</div></NuxtLink>
  </div>
  <button class="close-button" @click="isShown = !isShown">Menu</button>
</template>

<style>
  .container {
    top: 0;
    left: 0;
    position: fixed;
    height: 100%;
    width: 20rem;
    background: rgba(0, 0, 0, 0.733);
    display: flex;
    flex-direction: column;

    transition: left 0.2s;
  }

  .container:not(.show) {
    left: -22rem;
  }

  .link {
    margin: 1rem;
    font-size: 2rem;
    color: white;
    text-decoration: none
  }

  .link:hover {
    color: yellow;
  }
  
  a {
    text-decoration: none
  }

  .close-button {
    margin: 1rem;
    width: fit-content;
    z-index: 2;
    position: fixed;
    bottom: 0;
  }
</style>