<template>
  <q-page>
    <div class="text-h5 q-mt-md q-ml-md text-weight-bold">Создание заказа</div>
    <div class="row q-mt-md q-ml-md">
      <div class="q-mr-md col">
        <DeliveryInfo />
        <GoodsInfo class="q-mt-sm"/>
        <TransportInfo class="q-mt-sm"/>
        <Documents class="q-mt-sm"/>
      </div>
      <div class="col q-mr-md q-mr-md">
        <Map1/>
        <CreateOrderBiny class="q-mt-sm"/>
        <Tender class="q-mt-sm" @click="$router.push('/tender')"/>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import TransportInfo from "src/components/TransportInfo.vue";
import GoodsInfo from 'src/components/GoodsInfo.vue';
import DeliveryInfo from 'src/components/DeliveryInfo.vue';
import Documents from 'src/components/Documents.vue';
import Map1 from 'src/components/Map1.vue';
import CreateOrderBiny from 'src/components/CreateOrderBiny.vue';
import Tender from 'src/components/Tender.vue';

</script>
