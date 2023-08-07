<template>
  <div class="white-box bg-white flex">
    <q-list style="width: 50%">
      <q-item class="q-pb-none">
        <div class="text-subtitle1 text-weight-bold">Информация о доставке</div>
      </q-item>
      <q-item class="q-pt-none">
        <div class="text-subtitle1 gray-name">Отправитель</div>
      </q-item>
      <q-item class="q-py-none">
        <OrganizationInfo type="sender" style="width: 100%" />
      </q-item>
      <q-item>
        <div class="text-subtitle1 gray-name">Время погрузки</div>
      </q-item>
      <q-item class="q-pt-none">
        <Date />
        <Time1 />
      </q-item>
    </q-list>
    <q-list style="width: 50%">
      <q-item class="q-pb-none" style="min-height: 36px;"></q-item>
      <q-item class="q-pt-none">
        <div class="text-subtitle1 gray-name">Получатель</div>
      </q-item>
      <q-item class="q-py-none">
        <OrganizationInfo type="receiver" style="width: 100%" />
      </q-item>
      <q-item>
        <div class="text-subtitle1 gray-name">Время выгрузки</div>
      </q-item>
      <q-item class="q-pt-none">
        <Date />
        <Time1 />
      </q-item>
    </q-list>
  </div>
</template>

<script setup>
import OrganizationInfo from "src/components/OrganizationInfo.vue";
import Date from "src/components//Date.vue";
import Time1 from "src/components//Time.vue";
</script>
