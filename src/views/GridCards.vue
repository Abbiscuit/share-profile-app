<template>
  <div class="grid-garden">
    <div class="card" v-for="n in 15" :key="n">
      <h3 class="card__title">card title</h3>
      <div class="card-content">
        <p class="card-content__text">Lorem, ipsum dolor.</p>
        <button class="card-content__button">Register</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GridCards",
  components: {},
  data() {
    return {
      show: true,
    };
  },
};
</script>

<style lang="scss" scoped>
.grid-garden {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  justify-items: center;

  @media (max-width: 1400px) {
    grid-template-columns: repeat(3, 1fr);
  }

  @media (max-width: 1049px) {
    grid-template-columns: repeat(2, 1fr);
  }

  @media (max-width: 640px) {
    /* max-width: 300px;
    margin: 0 auto; */
    grid-template-columns: 1fr;
    gap: 16px;
  }

  .card {
    border-radius: 4px;
    border: 1px solid rgba(0, 0, 0, 0.25);
    padding: 16px;
    width: 300px;
    transition: 0.3s all;

    &:hover {
      transform: translateX(10px);
      background-color: rgb(224, 119, 119);
    }

    &__title {
      font-size: 24px;
      line-height: 1.5;
      margin: 0;
    }

    &-content {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-top: 24px;

      &__text {
        margin: 0;
      }

      &__button {
      }
    }
  }
}
</style>