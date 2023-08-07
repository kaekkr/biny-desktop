<template>
  <q-input outlined v-model="time" mask="time" :rules="['time']">
    <template v-slot:prepend>
      <q-icon name="img:/icons/desktop/create-order-menu/time.svg" class="cursor-pointer">
        <q-popup-proxy cover transition-show="scale" transition-hide="scale">
          <q-time v-model="time">
            <div class="row items-center justify-end">
              <q-btn v-close-popup label="Close" color="primary" flat />
            </div>
          </q-time>
        </q-popup-proxy>
      </q-icon>
    </template>
  </q-input>
</template>

<script setup>
import { ref } from "vue";

const time = ref(0);
</script>
