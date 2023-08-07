<template>
  <div class="white-box bg-white flex">
    <q-list class="flex q-py-md">
      <q-item class="q-py-none q-pr-xs">
        <q-item-section avatar>
          <q-icon name="img:/icons/desktop/create-order-menu/biny-logo.svg" />
        </q-item-section>
      </q-item>
      <q-item class="q-pa-none">
        <q-list>
          <q-item class="q-pa-none">
            <div class="text-h6">Создать заявку Biny</div>
          </q-item>
          <q-item class="q-pa-none">
            <div class="text-subtitle1">
              Моментальная заявка по справедливой цене, <br />автоматический
              подбор водителей
            </div>
          </q-item>
          <q-item class="q-pa-none q-mt-sm">
            <q-btn
              class="bg-primary text-white white-box"
              no-caps
              flat
              label="Создать заявку"
              style="width: 50%"
            />
          </q-item>
        </q-list>
      </q-item>
      <q-item class="q-pt-none">
        <q-list>
          <q-item>
            <div>1,200,000 ₸</div>
          </q-item>
          <q-item>
            <div>Цена 1 заявки: 1,200,000 ₸</div>
          </q-item>
          <q-item>
            <q-btn
              @click="decreaseNumberOfApplications"
              flat
              class="test"
              style="
                border-top-right-radius: 0px;
                border-bottom-right-radius: 0px;
                border-right: 0px;
              "
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
          </q-item>
        </q-list>
      </q-item>
    </q-list>
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
