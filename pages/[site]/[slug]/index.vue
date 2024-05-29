<script setup>
definePageMeta({
  title: "Site",
  layout: "empty",
});

throw createError({ statusCode: 404, statusMessage: "Page Not Found" });
</script>
<template>
  <div>Return 404</div>
</template>
