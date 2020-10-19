<template>
  <div v-html="markedContent"></div>
</template>

<script>
import marked from "marked";
import markDownSource from "./md/index.md";

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
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP&display=swap');
#app {
  font-family: 'Noto Sans JP', sans-serif;
}
table {
  width: 80%;
}
</style>