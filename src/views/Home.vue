<template>
  <div class="home">
    <h1>Test Application</h1>
    <button @click="show = !show">{{ show ? 'Close' : 'Open' }}</button>
    <transition name="fade">
      <div v-if="show">
        <GridCards />
      </div>
    </transition>
  </div>
</template>

<script>
import GridCards from "@/views/GridCards.vue";
export default {
  name: "Home",
  components: {
    GridCards,
  },
  data() {
    return {
      show: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>