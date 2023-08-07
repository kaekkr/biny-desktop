<template>
  <q-dialog>
    <q-card style="border-radius: 12px; position: relative; width: 616px">
      <q-card-section>
        <div class="text-h6">Добавить организацию</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-subtitl1 gray-name q-mb-xs">Название организации</div>
        <q-input v-model="search" outlined placeholder="Название организации">
        </q-input>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-subtitl1 gray-name q-mb-xs">Адрес</div>
        <q-input v-model="search" outlined placeholder="Выбрать на карте">
          <template v-slot:prepend>
            <q-icon
              name="img:/icons/desktop/create-order-menu/map.svg"
              size="xs"
            />
          </template>
        </q-input>
      </q-card-section>

      <q-card-section class="q-pt-none flex">
        <div style="width: 49%" class="q-mr-sm">
          <div class="text-subtitl1 gray-name q-mb-xs">Номер телефона</div>
          <q-input v-model="search" outlined placeholder="+7 (000) 000-00-00">
          </q-input>
        </div>
        <div style="width: 49%">
          <div class="text-subtitl1 gray-name q-mb-xs">E-mail</div>
          <q-input v-model="search" outlined placeholder="example@gmail.com">
          </q-input>
        </div>
      </q-card-section>

      <q-card-actions class="top-right">
        <q-btn
          flat
          icon="img:/icons/desktop/create-order-menu/exit.svg"
          v-close-popup
        />
      </q-card-actions>

      <q-card-actions class="q-ml-sm q-mb-sm">
        <q-btn
          flat
          class="bg-primary text-white white-box"
          label="Подтвердить"
          no-caps
          style="width: 40%"
          size="lg"
          v-close-popup
        />
        <q-btn
          flat
          class="bg-white text-primary"
          label="Отмена"
          no-caps
          size="lg"
          v-close-popup
        />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script setup></script>

<style scoped>
.top-right {
  position: absolute;
  top: 0;
  right: 0;
}
</style>
