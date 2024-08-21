<template>
  <div class="bg-theme-primary">
    <v-container class="py-16">
      <v-row no-gutters class="justify-center text-center align-center">
        <v-col md="6">
          <h1 class="fs-30 mb-6">
            China AI Policy Insights for Global Leaders
          </h1>
          <p>Comprehensive analysis and advisory on China's AI landscape</p>
          <v-text-field
            class="mt-10"
            append-inner-icon="mdi-magnify"
            density="compact"
            placeholder="Discover China AI policies and analysis"
            variant="solo"
            bg-color="white"
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
  </div>
  <div class="text-center text-black bg-light">
    <v-container class="py-16">
      <h1 class="text-theme-primary mb-16">China AI Database</h1>
      <v-row>
        <v-col
          v-for="(message, index) in blogPosts"
          :key="index"
          md="4"
          cols="12"
          class="px-md-16 mb-6"
        >
          <BlogPost :category="message" />
        </v-col>
      </v-row>
    </v-container>
  </div>
  <div class="bg-theme-primary-light">
    <v-container class="py-16">
      <h1 class="mb-16 text-center">Latest Analysis</h1>
      <v-row class="mb-16">
        <v-col md="6" cols="12">
          <v-img src="../assets/img-placeholder.png" class="mb-10"></v-img>
          <h3 class="mb-4">Analysis 2</h3>
          <p>Description...</p>
        </v-col>
        <v-col md="1" cols="0" class="border-opacity-75 border-e-sm"> </v-col>
        <v-col
          md="4"
          cols="12"
          class="pa-md-10 v-col-12 v-col-md-4 d-flex flex-column justify-space-between"
        >
          <div class="mb-16">
            <h3 class="mb-4">Analysis 2</h3>
            <p>Description...</p>
          </div>
          <div class="mb-16">
            <h3 class="mb-4">Analysis 2</h3>
            <p>Description...</p>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col md="4" cols="12" class="pa-6">
          <AnalysisPost />
        </v-col>
        <v-col md="4" cols="12" class="pa-6">
          <AnalysisPost />
        </v-col>
        <v-col md="4" cols="12" class="pa-6">
          <AnalysisPost />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import BlogPost from "./BlogPost.vue";

export default {
  components: {
    BlogPost,
  },
  data() {
    return {
      blogPosts: ["Government", "Market", "Private sector"],
    };
  },
};
</script>
