<template>
    <v-footer class="ma-0" height="auto" color="white">
      <v-container
        fluid
        class="white"
      >
        <v-row justify="center" align="center" class="pt-5">
          <v-col md="11" lg="11" sm="11" xl="11" cols="12">
            <v-card-text class="mx-0 px-0" style="height: 40px; position: relative">
              <v-fab-transition>
                <v-btn
                  aria-label="FAB Button"
                  style="margin-top:-30px"
                  color="white"
                  absolute
                  top
                  right
                  fab
                  @click="toTop"
                >
                  <v-icon>mdi-chevron-up</v-icon>
                </v-btn>
              </v-fab-transition>
              <h1
                class="google-font mb-0"
              >DevFest 2023</h1>
            </v-card-text> 
          </v-col>
        </v-row>
        <v-row justify="center" align="center" class="pb-5">
          <v-col md="11" sm="11" xl="11" lg="11" cols="12" class="">
            <a href="https://2022.devfestindia.com" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >DevFest 2022</a>
            <br class="hidden-md-and-up">
            
            <a href="https://developers.google.com/community/gdg" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >About GDG Program</a>
            <br class="hidden-md-and-up">
            <a href="https://www.womentechmakers.com/" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >About WTM Program</a>
            
  
            <br class="hidden-md-and-up">
            <!-- <router-link
              to="/faq"
              rel="noreferrer"
              class="mr-3 google-font grey--text text--darken-3"
              style="text-decoration:none;"
            >FAQ</router-link> -->
            <br class="hidden-md-and-up">
            <router-link to="/coc" style="text-decoration:none;" rel="noreferrer" class="mr-3 google-font grey--text text--darken-3">Code of conduct</router-link> 
            <br class="hidden-md-and-up">
            <a href="https://developers.google.com/community-guidelines" target="_blank"
              rel="noreferrer"
              class="mr-4 google-font grey--text text--darken-3"
              style="text-decoration:none;"
            >Community Guidelines</a>

              <br>

            <a href="https://merchant.razorpay.com/policy/MhLVr6S6qIxBR4/privacy" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >Privacy Policy</a>
            <br class="hidden-md-and-up">

            <a href="https://merchant.razorpay.com/policy/MhLVr6S6qIxBR4/terms" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >Terms & Conditions</a>
            <br class="hidden-md-and-up">

            <a href="https://merchant.razorpay.com/policy/MhLVr6S6qIxBR4/refund" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >Cancellation & Refund</a>
            <br class="hidden-md-and-up">

            <a href="https://merchant.razorpay.com/policy/MhLVr6S6qIxBR4/shipping" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >Shipping</a>
            <br class="hidden-md-and-up">

            <a href="https://merchant.razorpay.com/policy/MhLVr6S6qIxBR4/contact_us" target="_blank"
              rel="noreferrer"
              class="grey--text text--darken-3 mr-4 google-font"
              style="text-decoration:none;"
            >Contact Us</a>
            <br class="hidden-md-and-up">

          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </template>
  
  <script>
  export default {
    name: "AppFooter",
    methods: {
      toTop() {
        this.$vuetify.goTo(0);
      }
    }
  };
  </script>