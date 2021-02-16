<template>
  <svg
    version="1.1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    width="160.7px"
    height="215.9px"
    viewBox="0 0 160.7 215.9"
    style="overflow: visible; enable-background: new 0 0 160.7 215.9"
    xml:space="preserve"
    :class="{ outline }"
  >
    <polygon
      :class="['st0', { 'st0--outline': outline }]"
      points="155.8,72.1 112,52.9 56.6,100.8 93.8,114.2"
    />
    <polygon
      :class="['st0', { 'st0--outline': outline }]"
      points="147.2,130.2 103.4,114.2 47.9,150.4 84.7,161.7"
    />
    <polygon
      :class="['st1', { 'st1--outline': outline }]"
      points="48.3,169.2 77.3,1.5 28.4,61.1 1.5,195.3"
    />
    <polygon
      :class="['st0', { 'st0--outline': outline }]"
      points="142.4,196.1 48.3,169.2 1.5,195.3 79,214.4"
    />
    <path
      :class="['st2', { 'st2--outline': outline }]"
      d="M112,52.9l-3.6,25.8l0,0L150.9,96l0,0l-3.7,34.2l0,0l-43.8-16l0,0l-4.1,29.1l0,0l47.2,15.6l0,0l-4,37.2l0,0
	l-94.1-26.9l0,0l29-167.7l0,0l81.9,39.1l0,0l-3.4,31.4l0,0L112,52.9z"
    />
  </svg>
</template>

<script>
export default {
  name: "E",
  props: {
    outline: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
$gold: #F99D1C;
$yellow: #FDB913;
$gray: #414141;

svg {
  display: block;
  // scales with container
  width: 100%;
  height: auto;
}
svg.outline {
  position: absolute;
}
polygon,
path {
  stroke-linejoin: round;
}
.st0 {
  fill: $gray;
  stroke: #FFFFFF;
  stroke-width: 3;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
.st1 {
  fill: $yellow;
  stroke: #FFFFFF;
  stroke-width: 3;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
.st2 {
  fill: $gold;
  stroke: #FFFFFF;
  stroke-width: 3;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
// outline
.st0--outline {
  fill: none;
  stroke: #4f80ff;
  stroke-width: 1;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
.st1--outline {
  fill: none;
  stroke: #4f80ff;
  stroke-width: 1;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
.st2--outline {
  fill: none;
  stroke: #4f80ff;
  stroke-width: 1;
  /* stroke-linejoin: round; */
  stroke-miterlimit: 5;
}
</style>