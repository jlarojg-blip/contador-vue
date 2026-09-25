<script setup lang="ts">
import { ref } from 'vue'

const contador = ref<number>(0)

function aumentar() {
  contador.value++
}

function disminuir() {
  contador.value--
}
</script>

<template>
  <main class="contador">
    <h1>Contador</h1>

    <div class="numero" aria-live="polite">
      {{ contador }}
    </div>

    <div class="controles">
      <button
        class="menos"
        aria-label="Disminuir en uno"
        @click="disminuir"
      >
        −
      </button>

      <button
        class="mas"
        aria-label="Aumentar en uno"
        @click="aumentar"
      >
        +
      </button>
    </div>
  </main>
</template>