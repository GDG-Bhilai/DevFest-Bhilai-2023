<template>
  <v-app style="background-color: #F3F6FB">
    <appToolbarVue/>
    <appDrawerVue/>
    <v-main class="">
      <v-container fluid>
        <v-row justify="center" align="center">
          <v-col md="10">
            <v-slide-y-reverse-transition>
            <router-view v-show="show"/>
          </v-slide-y-reverse-transition>
          </v-col>
        </v-row>
      </v-container>

    <!-- <PopupTicket v-if="popupTriggers.timedTrigger"
    :TogglePopup = "() => TogglePopup('timedTrigger')">
      <h2>My Timed Popup</h2>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Suscipit asperiores optio illo nemo fugit eligendi delectus laboriosam quis totam amet ad quam repellendus laudantium voluptate itaque porro, ipsam ratione. Ad!
      </p>
    </PopupTicket> -->
     
    </v-main>
    <appFooterVue/>
  </v-app>
</template>

<script>
// import {ref} from 'vue';
import appDrawerVue from './components/core/appDrawer.vue';
import appFooterVue from './components/core/appFooter.vue';
import appToolbarVue from './components/core/appToolbar.vue';
// import PopupTicket from './components/home/PopupTicket.vue';
export default {
  name: 'App',
  components:{
    appToolbarVue,
    appFooterVue,
    appDrawerVue
  },
  data: () => ({
    show: false,
  }),
  created() {
    this.show = true;
  },
  // setup (){
  //   const popupTriggers = ref({
  //     timedTrigger: false
  //   });

  //   const TogglePopup = (trigger) => {
  //     popupTriggers.value[trigger] = !popupTriggers.value[trigger]
  //   }

  //   setTimeout(() => {
  //     popupTriggers.value.timedTrigger = true;
  //   }, 1000);
  //   return {
      
  //     PopupTicket,
  //     popupTriggers,
  //     TogglePopup
  //   }
  // }
};
</script>
