<!-- ./src/App.vue -->
<script setup>
import { ref } from "vue";
import CustomSlider from "./components/CustomSlider.vue";
import CustomMinMaxSlider from "./components/CustomMinMaxSlider.vue";

const slider1 = ref(100);
const slider2 = ref(0);

const sliderMin = ref(65);
const sliderMax = ref(150);
</script>
<template>
  <div class="slider-cont">
    <h3>Slider One: {{ slider1 }}</h3>
    <CustomSlider :max="500" v-model="slider1" />
  </div>

  <br />

  <div class="slider-cont">
    <h3>Slider Two: {{ slider2 }}</h3>
    <CustomSlider :min="-1" :max="1" :step="0.01" v-model="slider2" />
  </div>

  <br />

  <div class="slider-cont">
    <h3>Slider 3: {{ sliderMin }} - {{ sliderMax }}</h3>
    <CustomMinMaxSlider
      :min="65"
      :max="368"
      v-model:min-value="sliderMin"
      v-model:max-value="sliderMax"
    />
  </div>
</template>
