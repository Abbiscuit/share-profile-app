<template>
  <section class="orange">
    <div class="orange-text">
      <h2>
        甘い香りの
        <br />オレンジピールクッキー
      </h2>
      <p>オレンジピールのちょっとほろ苦い甘さと香りが美味しさを引き立ててくれる、やめられなくなるクッキーです。</p>
    </div>

    <figure class="orange-photo">
      <img src="@/assets/orange.jpg" alt />
    </figure>

    <div class="orange-sub">
      <img src="@/assets/bottle.jpg" alt />
      <p>
        可愛い小瓶に入ったパッケージはテーブルに置いておくだけでも絵になります。甘いものが苦手な人にもおすすめです。
        <router-link :to="{name: 'Hamburger'}">ハンバーガー</router-link>
        <router-link :to="{name: 'OrangePeel'}">ピールクッキー</router-link>
        <!-- <router-link to="/hamburger" >その他のサンプル</router-link> -->
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style lang="scss" scoped>
@import "@/styles/colors.scss";

.orange * {
  margin: 0;
}

.orange img {
  width: 100%;
  height: auto;
  vertical-align: bottom;
}

.orange-sub img {
  max-width: 120px;
}

/* Grid */
.orange {
  --side: 20px;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(2, auto);
  row-gap: 30px;
  margin: 0 var(--side) 30px;
}

.orange-photo {
  grid-column: 1 / -1;
  grid-row: 1;
  margin: 0 calc(var(--side) * -1);

  img {
    height: 100%;
    object-fit: cover;
    max-height: 600px;
  }
}

.orange-text {
  grid-column: span 5 / -1;
  grid-row: 1;
  justify-self: center;
  align-self: center;
  z-index: 10;
  padding: 40px 0;
  color: #fff;
  writing-mode: vertical-rl;
  text-shadow: 0px 0px 20px #000;

  display: grid;
  row-gap: 15px;
  justify-items: end;

  h2 {
    font-size: 40px;
    font-weight: 900;
    line-height: 1.5;
    padding-bottom: 20px;
  }

  p {
    height: 18em;
    font-size: 16px;
    line-height: 1.8;
  }
}

.orange-sub {
  grid-column: 1 / span 6;
  grid-row: 2;

  display: grid;
  grid-auto-flow: column;
  column-gap: 10px;

  p {
    font-size: 14px;
    line-height: 1.5;
  }

  img {
    border-radius: 8px;
  }

  a {
    display: block;
    color: $black;
  }
}

@media (max-width: 767px) {
  .orange-text {
    justify-self: end;
  }

  .orange-sub {
    grid-column: 1 / -1;
  }

  .orange::after {
    grid-column: 1 / -1;
    grid-row: 1;
    margin: 0 calc(var(--side) * -1);
    content: "";
    background-color: rgba(0, 0, 0, 0.4);
  }
}
</style>