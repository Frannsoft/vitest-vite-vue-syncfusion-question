<script setup lang="ts">
import { DialogComponent } from "@syncfusion/ej2-vue-popups";
import { ref } from 'vue'

const dialog = ref<InstanceType<typeof DialogComponent>>();

const isOpen = ref<boolean>(false);
</script>

<template>
  <div>
    <button @click="() => isOpen = !isOpen">Open dialog</button>
    <DialogComponent header="Title" :ref="dialog" :visible="isOpen" :close-on-escape="true">
      <p>some content</p>
    </DialogComponent>

  </div>
</template>
