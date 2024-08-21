<template>
  <div>
    <h3 class="text-start mx-md-6">{{ category }}</h3>
    <hr class="border-b-0" />
    <hr height="50px" class="d-inline" />
    <div class="mx-md-4 text-start">
      <v-img
        aspect-ratio="16/9"
        cover
        src="../assets/img-placeholder.png"
      ></v-img>
      <h4>Document 1</h4>
      <p>...</p>
      <hr class="my-3" />
      <h4>Document 2</h4>
      <p>...</p>
      <hr class="my-3" />
      <h4>Document 3</h4>
      <p>...</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    category: {
      type: String,
      required: true,
    },
  },
};
</script>
