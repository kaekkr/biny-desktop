<template>
  <q-layout view="hHh lpR fFf">
    <q-drawer
      show-if-above
      :mini="sideMenu"
      mini-to-overlay
      :width="325"
      :height="1048"
      class="bg-dark"
      style="border-top-right-radius: 12px; border-bottom-right-radius: 12px"
    >
      <q-scroll-area
        class="fit"
        :vertical-bar-style="{ background: 'white', height: '446px' }"
      >
        <q-list
          padding
          style="color: white; height: 100vh"
          class="flex column justify-between"
        >
          <div>
            <q-item>
              <q-btn
                v-if="sideMenu"
                flat
                @click="toggleSideMenu"
                size="md"
                icon="img:/icons/desktop/side-menu/hamburger.svg"
              >
              </q-btn>
              <div
                v-else
                class="flex justify-between items-center"
                style="width: 100%"
              >
                <q-icon
                  name="img:/icons/desktop/side-menu/biny-logo.svg"
                  size="xl"
                />
                <q-btn
                  @click="toggleSideMenu"
                  flat
                  icon="img:/icons/desktop/side-menu/exit.svg"
                  size="md"
                />
              </div>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/active-order.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Активные заказы </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/history-order.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> История заказов </q-item-section>
            </q-item>
            <q-separator />
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/transport-companies.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Транспортные компании </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/directions.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Направления </q-item-section>
            </q-item>
            <q-separator />
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/employees.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Сотрудники </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/document-flow.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Документооборот </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/invoice.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Счет-фактуры </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/analytics.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Аналитика </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/support.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> Поддержка </q-item-section>
            </q-item>
            <q-item v-ripple>
              <q-btn
                no-caps
                :class="
                  sideMenu
                    ? 'white-box bg-white text-black'
                    : 'test white-box bg-white text-black'
                "
                size="17px"
                to="/create-order"
              >
                <q-icon
                  name="img:/icons/desktop/side-menu/plus.svg"
                  size="12px"
                />
                <div class="q-ml-sm" v-if="!sideMenu">Создать заказ</div>
              </q-btn>
            </q-item>
          </div>

          <div>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/balance.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> 450 000 ₸ </q-item-section>
              <q-item-section
                ><q-btn
                  class="white-box bg-white text-black"
                  flat
                  label="Баланс"
              /></q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon
                  name="img:/icons/desktop/side-menu/user-logo.svg"
                  size="lg"
                />
              </q-item-section>
              <q-item-section> ТОО "GORILLA ASIA" </q-item-section>
              <q-item-section
                ><q-btn flat icon="img:/icons/desktop/side-menu/exit2.svg"
              /></q-item-section>
            </q-item>
          </div>
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";

const sideMenu = ref(true);

const toggleSideMenu = () => {
  sideMenu.value = !sideMenu.value;
};
</script>

<style scoped>
.test {
  width: 100%;
}
</style>
