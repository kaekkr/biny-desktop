<template>
  <div class="white-box bg-white">
    <q-list class="flex q-pt-sm q-pb-sm">
      <q-item style="max-height: 75px">
        <q-checkbox v-model="tender" />
      </q-item>
      <q-item class="block q-pl-none">
        <div class="text-h6">Разыграть тендер</div>
        <div class="text-subtitle1 gray-name">
          Разыграйте тендер между компаниями, которым вы доверяете
        </div>
        <q-list v-if="tender" class="q-mt-md">
          <q-separator class="q-mb-md" />
          <q-item class="q-pl-none q-pt-none block">
            <div class="text-subtitle1 gray-name">
              Выберите транспортные компании
            </div>
            <q-item class="q-pt-none q-pl-none">
              <q-btn no-caps flat class="test2">
                <div class="q-mr-md text-accent text-h6">+</div>
                <div class="text-subtitle1">Добавить компанию</div>
              </q-btn>
            </q-item>
          </q-item>
          <q-item class="q-pl-none block">
            <div class="text-subtitle1 gray-name">
              Время действия предложения
            </div>
            <q-list class="flex">
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="Нет" size="lg" />
              </q-item>
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="1 час" size="lg" />
              </q-item>
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="6 часов" size="lg" />
              </q-item>
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="12 часов" size="lg" />
              </q-item>
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="24 часа" size="lg" />
              </q-item>
              <q-item class="q-pl-none">
                <q-btn class="test" flat no-caps label="2 дня" size="lg" />
              </q-item>

              <q-item class="q-pl-none">
                <q-btn
                  class="white-box"
                  style="border: 2px solid #ecedee"
                  flat
                  no-caps
                  label="Другое"
                  size="lg"
                />
              </q-item>
            </q-list>
          </q-item>
          <q-item class="q-pl-none q-pt-none block">
            <div class="text-subtitle1 gray-name">
              Предложить ставку (необязательно)
            </div>
            <q-input outlined placeholder="0">
              <template v-slot:append>
                <q-icon
                  name="img:/icons/desktop/tender-menu/tenge.svg"
                  size="xs"
                />
              </template>
            </q-input>
          </q-item>
          <q-item class="q-pl-none q-pt-none block">
            <div class="text-subtitle1 gray-name">
              E-mail для получения уведомлений (необязательно)
            </div>
            <q-input outlined placeholder="example@gmail.com">
              <template v-slot:prepend>
                <q-icon
                  name="img:/icons/desktop/tender-menu/email.svg"
                  size="xs"
                />
              </template>
            </q-input>
          </q-item>
          <q-item class="q-pl-none q-mt-sm">
            <q-btn
              flat
              no-caps
              label="Отправить"
              class="bg-primary text-white white-box"
              size="lg"
            />
          </q-item>
        </q-list>
      </q-item>
    </q-list>
  </div>
</template>

<script setup>
import { ref } from "vue";

const tender = ref(false);
</script>

<style scoped>
.test2 {
  border: 2px dashed #dddee2;
  border-radius: 12px;
}
</style>
