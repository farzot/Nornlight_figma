 <template>
  <div class="md:w-full flex justify-center">
    <div class="bg-second rounded-[50px] mt-8 md:w-[1714px]">
      <div class="container">
        <swiper
          :pagination="true"
          :loop="true"
          :autoplay="{
            delay: 1500,
            disableOnInteraction: false,
          }"
          :modules="modules"
          class="mySwiper max-sm:w-[400px] transform transition duration-300 hover:scale-105 "
        >
          <swiper-slide v-for="(item, index) in items" :key="index">
            <div class="md:flex gap-[199px] mb-[47px] py-9 md:px-10 rounded-xl bg-[#F2F2F2] ">
              <p class="md:hidden w-[300px] text-3xl font-bold leading-9 mx-7">
                {{ item.title }}
              </p>
              <p class="bg-[#454545] py-1 px-4 mx-6 text-3xl rounded-full text-white md:hidden w-3/4">
                {{ item.date }}
              </p>
              <img src="/karusel.png" class="max-sm:hidden" alt="Candle" />
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css/navigation";
import "swiper/css"; 
import "swiper/css/pagination"; 
import { Autoplay, Pagination, Navigation } from "swiper/modules"; 
const modules = [Autoplay, Pagination, Navigation];

const items = [
  {
    title: "Скидка 15% на все подвесные светильники",
    date: "до 5 февраля",
  },
  {
    title: "Скидка 10% на настольные лампы",
    date: "до 10 февраля",
  },
  {
    title: "Скидка 20% на уличные светильники",
    date: "до 15 февраля",
  },
];
</script>

<style scoped>
.swiper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: grab;
}
.swiper:active {
  cursor: grabbing;
}


.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}
.swiper-pagination {
  position: absolute;
  right: 20px; 
  bottom: 20px; 
}
</style> 

