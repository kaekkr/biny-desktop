<template>
  <q-page>
    <div class="text-h5 q-mt-md q-ml-md text-weight-bold">
      Разыграть тендер или открыть аукцион
    </div>
    <div class="row q-mt-md q-ml-md">
      <div class="q-mr-md col">
        <CreateOrderBiny />
        <Tender2 class="q-mt-sm" />
        <Auction class="q-mt-sm" />
        <div class="white-box bg-white q-mt-md test" style="width: 32%">
          <q-btn
            no-caps
            flat
            label="Вернуться к созданию"
            icon="img:/icons/desktop/tender-menu/return-back.svg"
            size="lg"
            to="/create-order"
          />
        </div>
      </div>
      <div class="col q-mr-md q-mr-md">
        <Map1 />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import CreateOrderBiny from "src/components/CreateOrderBiny.vue";
import Map1 from "src/components/Map1.vue";
import Tender2 from "src/components/Tender2.vue";
import Auction from "src/components/Auction.vue";
</script>
