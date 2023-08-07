<template>
  <q-input
    outlined
    v-model="date"
    mask="date"
    :rules="['date']"
    class="q-mr-sm"
  >
    <template v-slot:prepend>
      <q-icon
        name="img:/icons/desktop/create-order-menu/calendar.svg"
        class="cursor-pointer"
      >
        <q-popup-proxy cover transition-show="scale" transition-hide="scale">
          <q-date v-model="date">
            <div class="row items-center justify-end">
              <q-btn v-close-popup label="Close" color="primary" flat />
            </div>
          </q-date>
        </q-popup-proxy>
      </q-icon>
    </template>
  </q-input>
</template>

<script setup>
import { ref } from "vue";

const date = ref("00.00.00");
</script>
