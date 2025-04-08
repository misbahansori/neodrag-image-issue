<script setup lang="ts">
import { vDraggable } from "@neodrag/vue";
</script>
<template>
  <div class="mx-auto max-w-4xl p-20">
    <p class="text-center text-gray-500">
      Drag the image to move it around. But it's not working correctly.
    </p>
    <img
      v-draggable
      :draggable="true"
      src="./assets/vue.svg"
      alt="Vue"
      class="size-40"
    />
    <div class="mt-24">
      <a
        href="https://github.com/misbahansori/neodrag-image-issue"
        class="text-blue-600 hover:underline"
      >
        Github Repo
      </a>
    </div>
  </div>
</template>
