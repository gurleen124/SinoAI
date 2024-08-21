<template>
  <v-footer class="py-16 bg-theme-primary" style="padding-inline: 128px">
    <v-row class="d-flex align-center">
      <v-col cols="12" md="2" class="ps-16">
        <v-img src="./../assets/sinoAI.png" :width="140" :height="192"></v-img
      ></v-col>
      <v-col cols="12" md="4">
        <span>
          SinoAI Advisory<br />51 East 14th Street<br />Chicago, IL 60605<br
        /></span>
        <v-icon class="me-1 pb-1" icon="mdi-email" size="18"></v-icon>
        inquiry@sinoaiadvisory.com
      </v-col>
      <v-col cols="12" md="6">
        <v-row no-gutters>
          <v-btn
            v-for="link in links"
            :key="link"
            class="mx-2"
            color="white"
            rounded="xl"
            variant="text"
          >
            {{ link }}
          </v-btn>
        </v-row></v-col
      >

      <v-col cols="12" class="mt-4">
        @{{ new Date().getFullYear() }} —
        <strong
          >SinoAI Advisory. All rights reserved. Privacy Policy and Terms of
          Use.</strong
        >
      </v-col>
    </v-row>
  </v-footer>
</template>
<script>
export default {
  name: "FooterComponent",

  data() {
    return {
      links: ["About", "Subscribe", "Contact Us"],
    };
  },
};
</script>
