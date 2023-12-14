<script lang="ts" setup>
defineProps({
  title: {
    type: String,
    default: "default"
  }
})

</script>
<template>
  <h1>{{ title }}</h1>
  <h2>
    <slot></slot>
  </h2>
</template>
<style lang="less" scoped></style>