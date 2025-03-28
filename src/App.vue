<script setup lang="ts">
import RadixSelect from "./components/RadixSelect.vue";
import RekaSelect from "./components/RekaSelect.vue";
</script>
<template>
  <div class="mx-auto max-w-4xl p-20">
    <div class="leading-relaxed flex flex-col gap-4">
      <h1 class="text-2xl font-semibold">
        Reka UI vs Radix Vue Select Value issue
      </h1>
      <p class="text-gray-500">
        When using the <code>Select</code> components from Reka UI, the
        <code>SelectValue</code> will not render element except for the text.
      </p>
      <RekaSelect />

      <hr class="my-2 border-gray-200" />

      <p class="text-gray-500">
        But when using the <code>Select</code> component from Radix Vue, the
        <code>SelectValue</code> will render everything including the image and
        text.
      </p>
      <RadixSelect />
    </div>
    <div class="flex flex-col gap-4 pt-6">
      <p class="text-gray-500">
        Note: The select implementation is the same for both components.
        <br />
        The only difference is the imports
      </p>
    </div>
  </div>
</template>
