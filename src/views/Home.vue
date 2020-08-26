<template>
  <div class="home">
    <button class="btn" @click="show = !show">{{ show ? 'Close' : 'Open' }}</button>
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

.btn {
  display: inline-block;
  /* margin: 0 auto; */
  background: #42b983;
  opacity: 0.85;
  border: none;
  padding: 8px 16px;
  color: #2c3e50;
  font-weight: 700;
  border-radius: 4px;
  outline: none;
  cursor: pointer;
  transition: opacity 0.3s;

  &:hover {
    opacity: 1;
  }
}
</style>