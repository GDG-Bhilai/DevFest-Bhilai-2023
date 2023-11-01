<template>
  <v-main class="pa-0 ma-0">
    <AppModal v-if="isDialogueVisible" @close="closeDialogue">
      <!-- <h2>My Dialogue</h2>
      <p>Dialogue content goes here.</p> -->
      <img src="src/views/modal.png"/>
    </AppModal>
    <!-- Hero -->
    <heroVue class="my-md-5 my-sm-5" />
    <!-- Hero -->

    <!-- Overview -->
    <overviewVue />
    <!-- Overview -->

    <!-- Technologies -->
    <technologiesVue class="mt-10" />
    <!-- Technologies -->

    <!-- Sponsors -->
    <homesponsors class="mt-10" />
    <!-- Sponsors -->

    <!-- Social -->
    <homeSocialVue class="my-10" />
    <!-- Social -->
  </v-main>
</template>

<script>
import heroVue from "@/components/home/hero.vue"
import overviewVue from "@/components/home/overview.vue"
import technologiesVue from "@/components/home/technologies.vue"
import homesponsors from "@/components/home/homeSponsors.vue"
import homeSocialVue from "@/components/home/homeSocial.vue"
import appModal from "@/components/core/appModal.vue"
import AppModal from "@/components/core/appModal.vue"

export default {
  name: "HomePage",
  components: {
    heroVue,
    overviewVue,
    technologiesVue,
    homesponsors,
    homeSocialVue,
    appModal,
    AppModal,
  },
  data() {
    return {
      isDialogueVisible: false,
    }
  },
  methods: {
    showDialogue() {
      this.isDialogueVisible = true
    },
    closeDialogue() {
      this.isDialogueVisible = false
    },
  },
  mounted() {
    setTimeout(() => {
      this.isDialogueVisible = true
    }, 2000)
  },
}
</script>
