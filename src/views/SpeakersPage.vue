<template>
  <v-main class="pa-0 ma-0">
    <v-container fluid class="my-10">
      <v-row>
        <v-col md="12" sm="12" cols="12" class="text-center  google-font">
          <p
            class="google-font gdg-h1 mb-2 grey--text text--darken-4"
            style="font-size: 220%"
          >
            <!-- Speakers -->
          </p>
          <p style="font-size: 250%">
            The anticipation is building! We're about to unveil our exceptional lineup of speakers. Get ready to be inspired by the best in the industry. Stay tuned for updates!
          </p>
        </v-col>
        <v-col md="2" cols="6" sm="3" v-for="(item, index) in speakersInfo" :key="index">
          <speakerCardVue :item="item"/>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
import speakerCardVue from "@/components/speakers/speakerCard.vue";
import speakersJSON from "@/assets/data/speakers.json";

export default {
  name: "SpeakersPages",
  components: {
    speakerCardVue,
  },
  data: () => ({
    speakersInfo: speakersJSON,
  }),
};
</script>

<style>
</style>