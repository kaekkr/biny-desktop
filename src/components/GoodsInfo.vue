<template>
  <div class="white-box bg-white">
    <div class="text-subtitle1 text-weight-bold row q-pl-md q-pt-md">
      Информация о грузе (на 1 заявку)
    </div>
    <q-list class="row">
      <q-item class="q-py-none col" style="display: block">
        <div class="text-subtitle1 gray-name">Обьём</div>
        <q-input
          v-model="volume"
          outlined
          placeholder="0"
        >
          <template v-slot:append>
            <div class="text-subtitle1">м3</div>
          </template>
        </q-input>
      </q-item>
      <q-item class="q-py-none q-pl-none col" style="display: block">
        <div class="text-subtitle1 gray-name">Вес</div>
        <q-input
          v-model="volume"
          outlined
          class="q-ml-none"
          placeholder="0"
        >
          <template v-slot:append>
            <div class="text-subtitle1">тонн</div>
          </template>
        </q-input>
      </q-item>
      <q-item class="q-py-none col-6" style="display: block">
        <div class="text-subtitle1 gray-name">Категория груза</div>
        <q-select
          outlined
          v-model="model"
          :options="options"
          display-value="Продукты питания"
        />
      </q-item>
    </q-list>
    <q-list class="row q-pb-md">
      <q-item class="col-6" style="display: block">
        <div class="text-subtitle1 gray-name">Описание</div>
        <q-input
          outlined
          placeholder="Например, особые условия хранения"
        />
      </q-item>
      <q-item class="flex items-center col q-pb-none q-pt-lg">
        <q-checkbox v-model="dangerousGoods" />
        <div class="text-subtitle1">Опасный груз</div>
      </q-item>
    </q-list>
  </div>
</template>

<script setup>
import { ref } from "vue";

const dangerousGoods = ref(false);
const options = ['Продукты питания']
</script>
