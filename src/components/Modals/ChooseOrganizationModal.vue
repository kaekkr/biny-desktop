<template>

  <q-dialog>
    <AddOrganizationModal v-model="addOrganizationModal"/>
    <q-card style="border-radius: 12px; position: relative; width: 616px">
      <q-card-section>
        <div class="text-h6">Выбрать организацию</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <q-input
        v-model="search"
        outlined
        placeholder="Search"
      >
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <OrganizationInfo type="choose"/>
      </q-card-section>

      <q-card-actions class="top-right">
        <q-btn flat icon="img:/icons/desktop/create-order-menu/exit.svg" v-close-popup />
      </q-card-actions>

      <q-card-actions>
        <q-btn @click="openAddOrganizationModal" flat class="bg-primary text-white white-box" label="Добавить организацию" no-caps style="width: 100%"/>
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script setup>
import {ref} from 'vue';
import OrganizationInfo from '../OrganizationInfo.vue';
import AddOrganizationModal from './AddOrganizationModal.vue';

const addOrganizationModal = ref(false);

const openAddOrganizationModal = () => {
  addOrganizationModal.value = true;
}


</script>

<style scoped>

.top-right {
  position: absolute;
  top: 0px;
  right: -15px;
  bottom: 270px;
}

</style>
