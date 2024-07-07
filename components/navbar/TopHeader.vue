<script setup>
const isTrue = ref(false);

const showModal = () => {
  isTrue.value = true;
};
const hideModal = () => {
  isTrue.value = false;
};
</script>

<template>
  <MainModalka v-if="isTrue" :hideModal="hideModal" />
  <div class="max-sm:hidden container py-3">
    <div class="flex justify-between items-center .menu-item.selected">
      <div class="flex gap-4 .button-hover">
        <nuxt-link to="/AboutUs">О компании</nuxt-link>
        <nuxt-link to="/Delivery">Доставка и оплата</nuxt-link>
        <nuxt-link to="/Return">Возврат</nuxt-link>
        <nuxt-link to="/Gaurantee">Гарантии</nuxt-link>
        <nuxt-link to="/Contacts">Контакты</nuxt-link>
        <nuxt-link to="/Blog">Блог</nuxt-link>
      </div>
      <div class="flex gap-4 items-center">
        <p class="text-[#454545] font-semibold">8 (800) 890-46-56</p>
        <button @click="showModal">Заказать звонок</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.button-hover {
  background-color: white;
  transition: background-color 0.3s ease;
}

.button-hover:hover {
  background-color: yellow;
}</style>
