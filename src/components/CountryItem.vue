<template>
  <div @click="toggleDetails()">
    <div class="name">Country: {{ country.name.official}}</div>
    <div class="image-wrapper">
      <img :src="country.flags.svg" alt />
    </div>

    <div v-if="isVisible" class="details">
        details
      <!-- diplay country details in a specific component or create a specific view that display a single component -> vue router param + api /name endpoint
      -->
    </div>
  </div>
</template>

<script>
export default {
  name: "CountryItem",
  props: {
    country: Object
  },
  data() {
    return {
      isVisible: false
    };
  },
  methods: {
    toggleDetails: function() {
      this.isVisible = !this.isVisible;
    }
  }
};
</script>

<style scoped>
img {
  width: 200px;
}
</style>

