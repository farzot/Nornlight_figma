<script setup>
const data = ref([
  {
    numbers: 170,
    text: "Товаров",
  },
  {
    numbers: 1000,
    text: "Довольных покупателей",
  },
  {
    numbers: 170,
    text: "Товаров",
  },
]);
</script>

<template>
  <div class="container py-9 max-sm:px-3">
    <div class="flex items-center gap-3">
      <nuxt-link to="/" class="text-[#454545] py-4">Главная ></nuxt-link>
      <p>О компании</p>
    </div>
    <div class="md:flex gap-10">
      <div class="md:w-1/3">
        <h2 class="text-[#454545] text-6xl font-bold py-5">О компании</h2>
        <div v-for="(item, index) in data" :key="index" class="py-3">
          <div
            class="flex flex-col justify-between bg-[#F2F2F2] gap-20 p-4 rounded-lg transform transition duration-300 hover:scale-105 hover:bg-gray-200"
          >
            <p class="text-4xl font-bold">{{ item.numbers }}+</p>
            <p>{{ item.text }}</p>
          </div>
        </div>
      </div>
      <div class="md:w-2/3 text-[20px] text-[#454545]">
        <p class="md:w-[90%]">
          Интернет-магазин NORNLIGHT предлагает широкий ассортимент светильников
          для освещения вашего дома или офиса. У нас вы найдете разнообразные
          модели светильников, от современных и стильных до классических и
          элегантных. Мы предлагаем качественные и надежные светильники от
          лучших производителей, которые подарят вам комфорт и уют. <br /><br />
          Покупая светильники в нашем интернет-магазине, вы получаете отличное
          соотношение цены и качества. Мы осуществляем доставку по всей России,
          чтобы каждый клиент мог насладиться прекрасным светом и удобством
          покупки онлайн. Обратитесь к нам сегодня и превратите ваш дом в оазис
          тепла и света с NORNLIGHT! <br /><br />Интернет-магазин NORNLIGHT
          предлагает широкий ассортимент светильников для освещения вашего дома
          или офиса. У нас вы найдете разнообразные модели светильников, от
          современных и стильных до классических и элегантных. Мы предлагаем
          качественные и надежные светильники от лучших производителей, которые
          подарят вам комфорт и уют. <br /><br />Покупая светильники в нашем
          интернет-магазине, вы получаете отличное соотношение цены и качества.
          Мы осуществляем доставку по всей России, чтобы каждый клиент мог
          насладиться прекрасным светом и удобством покупки онлайн. Обратитесь к
          нам сегодня и превратите ваш дом в оазис тепла и света с NORNLIGHT!
        </p>
      </div>
    </div>
    <MainMarque class="" />
    <MainBlog />
    <MainBlog2 />
  </div>
</template>

<style scoped></style>
