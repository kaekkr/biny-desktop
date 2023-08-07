<template>
  <div class="flex">
    <q-btn
      @click="decreaseNumberOfApplications"
      flat
      class="test"
      style="
        border-top-right-radius: 0px;
        border-bottom-right-radius: 0px;
        border-right: 0px;
      "
      size="lg"
    >
      <div>-</div>
    </q-btn>
    <div
      class="test flex items-center text-subtitle1"
      style="border-radius: 0px; border-left: 0px; border-right: 0px"
    >
      {{ numberOfApplications }}
    </div>
    <q-btn
      @click="increaseNumberOfApplications"
      flat
      class="test"
      style="
        border-top-left-radius: 0px;
        border-bottom-left-radius: 0px;
        border-left: 0px;
      "
    >
      <div>+</div>
    </q-btn>
  </div>
</template>

<script setup>
import { ref } from "vue";

const numberOfApplications = ref(0);

const increaseNumberOfApplications = () => {
  numberOfApplications.value++;
};

const decreaseNumberOfApplications = () => {
  numberOfApplications.value--;
};
</script>
