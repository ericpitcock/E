<template>
  <svg
    x="0px"
    y="0px"
    width="160.7px"
    height="215.9px"
    viewBox="0 0 160.7 215.9"
    :class="{ outline }"
  >
    <polygon
      class="shadow"
      points="155.8,72.1 112,52.9 56.6,100.8 93.8,114.2"
    />
    <polygon
      class="shadow"
      points="147.2,130.2 103.4,114.2 47.9,150.4 84.7,161.7"
    />
    <polygon
      class="highlight"
      points="48.3,169.2 77.3,1.5 28.4,61.1 1.5,195.3"
    />
    <polygon
      class="shadow"
      points="142.4,196.1 48.3,169.2 1.5,195.3 79,214.4"
    />
    <path
      class="face"
      d="M112,52.9l-3.6,25.8l0,0L150.9,96l0,0l-3.7,34.2l0,0l-43.8-16l0,0l-4.1,29.1l0,0l47.2,15.6l0,0l-4,37.2l0,0
	l-94.1-26.9l0,0l29-167.7l0,0l81.9,39.1l0,0l-3.4,31.4l0,0L112,52.9z"
    />
  </svg>
</template>

<script>
  export default {
    name: 'E',
    props: {
      outline: {
        type: Boolean,
        default: false
      }
    }
  }
</script>

<style lang="scss" scoped>
  $gold: #f99d1c;
  $yellow: #fdb913;
  $gray: #414141;
  $white: #fff;

  svg {
    display: block;
    // scales with container
    width: 100%;
    height: auto;
  }
  polygon,
  path {
    stroke: $white;
    stroke-width: 3;
    stroke-linejoin: round;
    stroke-miterlimit: 5;
  }
  .shadow {
    fill: $gray;
  }
  .highlight {
    fill: $yellow;
  }
  .face {
    fill: $gold;
  }
  svg.outline {
    position: absolute;
    .shadow,
    .highlight,
    .face {
      fill: none;
      stroke: #4f80ff;
      stroke-width: 1;
    }
  }
</style>
