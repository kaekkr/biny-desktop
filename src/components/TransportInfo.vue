<template>
  <div class="white-box bg-white">
    <div class="text-subtitle1 text-weight-bold row q-pl-md q-pt-md">
      Информация о транспорте
    </div>
    <q-list class="row">
      <q-item class="q-py-none col" style="display: block">
        <div class="text-subtitle1 gray-name">Тип транспорта</div>
        <q-btn
          class="test"
          style="
            border-top-right-radius: 0px;
            border-bottom-right-radius: 0px;
            border-right: 0px;
            width: 25%;
          "
          flat
          size="lg"
          no-caps
        >
          <div>
            <q-icon name="img:/icons/desktop/create-order-menu/tent.svg" />
            <div>Test</div>
          </div>
        </q-btn>
        <q-btn
          class="test"
          style="border-radius: 0px; border-right: 0px; width: 25%"
          flat
          size="lg"
        >
          <div>
            <q-icon name="img:/icons/desktop/create-order-menu/covered.svg" />
            <div>Test</div>
          </div>
        </q-btn>
        <q-btn
          class="test"
          style="border-radius: 0px; width: 25%"
          flat
          size="lg"
        >
          <div>
            <q-icon name="img:/icons/desktop/create-order-menu/isoterm.svg" />
            <div>Test</div>
          </div>
        </q-btn>
        <q-btn
          class="test"
          style="
            border-top-left-radius: 0px;
            border-bottom-left-radius: 0px;
            border-left: 0px;
            width: 25%;
          "
          flat
          size="lg"
        >
          <div>
            <q-icon name="img:/icons/desktop/create-order-menu/refrijerator.svg" />
            <div>Test</div>
          </div>
        </q-btn>
      </q-item>
    </q-list>
    <q-list class="row q-pb-md q-mt-sm">
      <q-item class="q-pt-none col" style="display: block">
        <div class="text-subtitle1 gray-name">Количество</div>
        <div class="flex items-center">
          <Counter class="q-mr-sm" />
          <div class="text-subtitle1">Заявок</div>
        </div>
      </q-item>
      <q-item class="col" style="display: block">
        <div class="text-subtitle1 gray-name">Температурный режим</div>
        <q-select
          outlined
          v-model="model"
          :options="options"
          display-value="от 0°C до 5°C"
        />
      </q-item>
    </q-list>
  </div>
</template>

<script setup>
import Counter from "src/components/Counter.vue";

const options = ["от 0°C до 5°C"];
</script>
