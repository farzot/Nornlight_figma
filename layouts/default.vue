<script setup>
useHead({
  title: "Habibulloyev Farzot",
  link: {
    href: "https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css",
    rel: "stylesheet",
  },
});
</script>

<template>
  <navbarTopHeader />
  <Navbar />
  <slot />
  <Footer />
</template>

<style scoped></style>
