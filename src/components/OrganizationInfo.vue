<template>
  <ChooseOrganizationModal v-model="chooseOrganizationModal" />

  <q-list class="test flex" style="position: relative">
    <q-item
      v-if="type !== 'choose'"
      class="q-py-none q-pr-none col-1"
      style="width: 12%"
    >
      <q-item-section avatar class="q-pr-none">
        <q-icon
          :name="
            type === 'sender'
              ? 'img:/icons/desktop/create-order-menu/sender.svg'
              : 'img:/icons/desktop/create-order-menu/receiver.svg'
          "
        />
      </q-item-section>
    </q-item>
    <q-item class="q-pl-sm" :class="type === 'choose' ? 'q-py-none' : 'q-pa-none'">
      <q-list>
        <q-item class="q-pb-none q-pl-none">
          <div class="text-h6">КазПочта</div>
        </q-item>
        <q-item class="q-pa-none">
          <div class="text-subtitle1">г. Атырау ул, Баймуханова 70а</div>
        </q-item>
        <q-item class="q-pt-none q-pr-none q-pl-none">
          <div class="text-subtitle1 gray-name q-mr-sm">+79990009999</div>
          <div class="text-subtitle1 gray-name">kazpost@gmail.com</div>
        </q-item>
      </q-list>
    </q-item>
    <q-item class="q-pa-none top-right">
      <q-btn
        @click="openChooseOrganizationModal"
        flat
        :icon="
          type === 'choose'
            ? 'img:/icons/desktop/create-order-menu/three-dots.svg'
            : 'img:/icons/desktop/create-order-menu/change-details.svg'
        "
        size="sm"
      />
    </q-item>
  </q-list>
</template>

<script setup>
import { ref } from "vue";
import ChooseOrganizationModal from "src/components/Modals/ChooseOrganizationModal.vue";

const props = defineProps(["type"]);
const chooseOrganizationModal = ref(false);

const openChooseOrganizationModal = () => {
  if (props.type === 'choose') return;
  chooseOrganizationModal.value = true;
  console.log(chooseOrganizationModal.value);
};
</script>

<style scoped>
.top-right {
  position: absolute;
  top: -60px;
  right: -5px;
  bottom: 0px;
}
</style>
