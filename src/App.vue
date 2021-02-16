<template>
  <div id="app">
    <div
      :class="['bounding-box', { 'bounding-box--selected': selected }]"
      @click="selected = !selected"
    >
      <e :outline="true" v-if="selected" />
      <e :outline="false" />
    </div>
  </div>
</template>

<script>
import E from "@/components/E";

export default {
  name: "App",
  data: () => ({
    selected: false,
  }),
  components: {
    E,
  },
};
</script>

<style lang="scss">
$blue: #4f80ff;

body {
  margin: 0;
  /* background: lightgray; */
}
#app {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bounding-box {
  position: relative;
  border: 1px solid transparent;
  &--selected {
    border-color: $blue;
  }
}
</style>
