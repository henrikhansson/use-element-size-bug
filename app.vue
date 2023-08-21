<template>
  <div ref="container">
    <h1>{{ width }}</h1>
  </div>
</template>

<script setup lang="ts">

const container = ref();
const { width } = useElementSize( container );

onMounted(() => {
  console.log(`VueUse: ${ width.value }`);
  console.log(`offsetWidth: ${ container.value.offsetWidth }`);
});

</script>