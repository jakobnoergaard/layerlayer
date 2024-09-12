<script setup lang="ts">
const { myLayer } = useAppConfig()
</script>

<template>
  <div>
    <h1>Hello Jakob!</h1>
    <pre>{{ myLayer }}</pre>
    <div style="color: red">
      <slot></slot>
    </div>
  </div>
</template>
