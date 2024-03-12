<template>
<div class="font-bold bg-blue-300 p-8 flex flex-col gap-8 w-64" >
    <div class="text-xl">{{ greeting }}</div>
    <div v-if="visible">
        <slot ></slot>
    </div>
    <button class="text-sm" 
        @click="visible=!visible">
        {{visible ? "Hide" : "Show"}}
    </button>
</div>
</template>
<script setup lang="ts">
import { ref } from 'vue';
import { useHotKeys } from '../composables/useHotKeys';

const { 
    greeting
} = defineProps<{ greeting: string }>();

const visible = ref(true)

const { keys, keyboardEvent } = useHotKeys();


</script>
