<template>
  <div class="flex flex-col gap-2 items-center">
    <Greeter greeting="Grüße">
      <p class="text-xs">Lorem ipsum hallo hallo</p>
    </Greeter>
  </div>
</template>
<script setup lang="ts">
import Greeter from './components/Greeter.vue'
</script>
