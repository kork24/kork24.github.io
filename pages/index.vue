<template>
  <div class="page coop-overfishing">
    <div class="coop-overfishing-header">
      <h2><span>Salmon Run</span></h2>
      <h3><span>Overfishing 200</span></h3>
    </div>
    <div class="coop-overfishing-list-wrapper">
      <div class="coop-overfishing-list">
        <div v-html="markedContent"></div>
      </div>
    </div>
  </div>
</template>

<script>
import marked from "marked";
import markDownSource from "~/pages/md/index.md";

export default {
  computed: {
    source() {
      return markDownSource;
    },
    markedContent() {
      return marked(this.source);
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+JP&display=swap");
#app {
  font-family: "Noto Sans JP", sans-serif;
}

html {
  height: 100%;
}

div {
  display: block;
}

.page {
  min-height: 100%;
  box-sizing: border-box;
}

.container {
  width: 100%;
  max-width: 100%;
  padding: 0;
}

.coop-overfishing-header {
  position: relative;
  text-align: center;
  padding: 16px 0 30px;
}

.coop-overfishing h2 {
  position: relative;
  background-image: url("https://app.splatoon2.nintendo.net/images/bundled/a185b309f5cdad94942849070de04ce2.png");
  background-size: contain;
  width: 332px;
  margin: 0 auto;
  height: 112.5px;
  z-index: 1;
}

.coop-overfishing h2 span {
  display: none;
  position: absolute !important;
  clip: rect(1, 1, 1, 1);
}

.coop-overfishing {
  position: relative;
  background-image: url("https://app.splatoon2.nintendo.net/images/bundled/8c15ceb605300fbc22963fabcb09fb22.png");
  background-size: 255px 127px;
  background-repeat: repeat;
  overflow: hidden;
  width: 100%;
}

.coop-overfishing-header h3 {
  font-family: "Splatfont";
  min-width: 200px;
  background-position-x: 50%;
  background-position-y: center;
  box-sizing: border-box;
  color: #ff5033;
}

.coop-overfishing-header h3:after {
  background-position: 100% center;
  width: 42px;
  content: "";

  display: inline-block;
  background-size: 488px 52px;
  background-image: url("https://app.splatoon2.nintendo.net/images/bundled/cc7454b6eb6b8e16852ed21f00e0fd40.png");
  height: 52px;
  vertical-align: middle;
}

.coop-overfishing-header h3:before {
  background-position: 0px center;
  width: 42px;
  content: "";

  display: inline-block;
  background-image: url("https://app.splatoon2.nintendo.net/images/bundled/cc7454b6eb6b8e16852ed21f00e0fd40.png");
  background-size: 488px 52px;
  height: 52px;
  vertical-align: middle;
}

.coop-overfishing-header h3 span {
  padding-top: 16px;
  min-width: 200px;
  background-position: 50%;
  box-sizing: border-box;

  display: inline-block;
  background-image: url("https://app.splatoon2.nintendo.net/images/bundled/cc7454b6eb6b8e16852ed21f00e0fd40.png");
  background-size: 488px 52px;
  height: 52px;
  vertical-align: middle;
}

.coop-overfishing-list-wrapper {
  position: relative;
  background: rgba(0, 0, 0, 0.33);
  padding-top: 16px;
  padding-bottom: 90px;
  padding-bottom: calc(constant(safe-area-inset-bottom) + 90px);
  padding-bottom: calc(env(safe-area-inset-bottom) + 90px);
  z-index: 1;
}

.coop-overfishing-list-wrapper:before {
  background: rgba(0, 0, 0, 0.33);
  content: "";
  position: absolute;
  width: 100%;
  height: 20px;
  margin-top: -36px;
  left: 0;
  -webkit-mask-image: url("~@/static/3ff65812f7fc0aff176df4c78172691c.png");
  mask-image: url(https://app.splatoon2.nintendo.net/images/bundled/3ff65812f7fc0aff176df4c78172691c.png);
  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat;
  -webkit-mask-size: 100% 100%;
  mask-size: 100% 100%;
}

.coop-overfishing-list {
  font-family: "Splatfont";
  max-width: 800px;
  /* max-width: 570px; */
  margin: 0 auto;
  padding: 0 12px;
}

.coop-overfishing-list table {
  width: 100%;
  background: rgba(0, 0, 0, 0.8);
  background-image: url(https://app.splatoon2.nintendo.net/images/bundled/b24ee02521f18ebe1bf8b05e1396c3dc.png);
  background-repeat: repeat;
  background-size: 60px 60px;
  padding: 30px;
  border-radius: 20px;
  margin-bottom: 24px;
}

h1,
h2,
h3 {
  margin: 0;
  padding: 0;
}
</style>

<style lang="scss">
@font-face {
  font-family: "SplatFont";
  src: url("~@/assets/fonts/Splatfont.woff") format("woff"),
    url("~@/assets/fonts/Splatfont.woff2") format("woff2");
}

@font-face {
  font-family: "SplatFont2";
  src: url("~@/assets/fonts/Splatfont2.woff") format("woff"),
    url("~@/assets/fonts/Splatfont2.woff2") format("woff2");
}

div {
  .coop-overfishing-title {
    text-align: center;
    font-size: 25px;
  }
  body {
     font-size: 1.5vw;
  }
p#vw {
  font-size: 5vw;
}
p#vh {
  font-size: 5vh;
}
    &.names {
      color: white;
    }

    &.normal {
      color: yellowgreen;
    }

    &.golden {
      color: yellow;
    }
  }

  table {
    text-align: left;
    max-width: 800px;
    table-layout: fixed;
  }
  table td 
  {
    @media screen and (max-width: 600px) {
    white-space: nowrap;
    font-size: 2.5vw;

    }
    //white-space: nowrap;
    padding: 0 5px 0 5px;
    // width: 50px;
  }
</style>