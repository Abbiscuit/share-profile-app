<template>
  <div class="peel">
    <figure class="peel-photo">
      <img src="@/assets/orange-circle.png" alt />
    </figure>

    <div class="peel-jp">
      <h2>
        甘い香りの
        <br />オレンジピールクッキー
      </h2>
      <p>オレンジの皮のほんのり苦味がアクセント</p>
      <p>オレンジの皮を砂糖で煮込んだ一品です。クッキー生地と合わせることでオレンジの豊潤な香りと甘みを楽しむことができます。</p>
    </div>

    <aside class="peel-jp-memo">賞味期限は1年です。密閉度の高い瓶に入れて保管すると美味しさを保つことができます。</aside>

    <div class="peel-en">
      <h2>ORANGE PEEL COOKIES</h2>
      <p>The bitter taste of the orange peel is accented.</p>
      <p>Orange peel cooked with sugar. You can enjoy the rich aroma and sweetness of orange in the cookie.</p>
    </div>

    <aside
      class="peel-en-memo"
    >The expiration date is 1 year. Keeping it in a bottle with a high sealability.</aside>
  </div>
</template>

<script>
export default {
  name: "OrangePeel",
};
</script>

<style lang="scss" scoped>
.peel * {
  margin: 0;
}

.peel {
  --sideLR: 20px;
  --sideTB: 40px;

  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 170px auto 100px;
  margin: var(--sideTB) var(--sideLR);

  img {
    width: 100%;
    height: auto;
    vertical-align: bottom;
  }

  &-photo {
    grid-column: 1 / -1;
    grid-row: 2;
    justify-self: center;
    align-self: center;
    width: 60%;
  }

  &-jp {
    grid-column: 2;
    grid-row: 1 / 3;
    justify-self: end;
    align-self: start;
    writing-mode: vertical-rl;

    display: grid;
    row-gap: 15px;

    h2 {
      font-size: 42px;
      font-weight: 900;
      line-height: 1.2;
    }

    p:nth-of-type(1) {
      font-size: 16px;
      font-weight: 700;
      color: #444;
    }

    p:nth-of-type(2) {
      font-size: 14px;
      font-weight: 300;
      line-height: 1.8;
      height: 12em;
    }
  }

  &-jp-memo {
    grid-column: 2;
    grid-row: 3;

    justify-self: end;
    align-self: end;
    width: 200px;
    padding: 10px;
    box-sizing: border-box;
    border: 1px solid #aaa;
    font-size: 12px;
    font-weight: 200;
    line-height: 1.5;
  }

  &-en {
    grid-column: 1;
    grid-row: 1 / 3;
    justify-self: start;
    align-self: start;
    color: #fff;
    font-family: "Montserrat", sans-serif;
    display: grid;
    grid-row-gap: 15px;

    h2 {
      font-size: 40px;
      font-weight: 700;
    }

    p:nth-of-type(1) {
      font-size: 16px;
      font-weight: 500;
    }

    p:nth-of-type(2) {
      font-size: 14px;
      font-weight: 300;
      width: 50%;
    }
  }

  &-en-memo {
    grid-column: 1;
    grid-row: 3;
    color: #fff;
    justify-self: start;
    align-self: end;
    width: 200px;
    padding: 10px;
    box-sizing: border-box;
    border: 1px solid #aaa;
    font-family: "Montserrat", sans-serif;
    font-size: 12px;
    font-weight: 300;
    line-height: 1.5;
  }

  &::after {
    grid-column: 1;
    grid-row: 1 / -1;
    z-index: -1;
    content: "";
    background-color: #222;
    margin-left: calc(var(--sideLR) * -1);
    margin-top: calc(var(--sideTB) * -1);
    margin-bottom: calc(var(--sideTB) * -1);
  }
}

@media (min-width: 1000px) {
  .peel {
    --sideLR: calc((100vw - 960px) / 2);
  }
}

@media (max-width: 767px) {
  .peel {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(6, auto);

    &-jp {
      grid-column: 1;
      grid-row: 1;
      writing-mode: horizontal-tb;

      p:nth-of-type(2) {
        height: auto;
      }
    }

    &-jp-memo {
      grid-column: 1;
      grid-row: 2;
      justify-self: stretch;
      width: auto;
      margin-top: 15px;
    }

    &-photo {
      grid-column: 1;
      grid-row: 3 / 5;
      width: 80%;
      margin: 30px 0;
    }

    &-en {
      grid-column: 1;
      grid-row: 5;

      p:nth-of-type(2) {
        width: auto;
      }
    }

    &-en-memo {
      grid-column: 1;
      grid-row: 6;
      justify-self: stretch;
      width: auto;
      margin-top: 15px;
    }

    &::after {
      grid-column: 1;
      grid-row: 4 / -1;
      margin-top: 0;
      margin-right: calc(var(--sideLR) * -1);
    }
  }
}
</style>