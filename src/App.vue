<template>
  <div id="app">
    <drag-it-dude
      @activated="handleActivated"
      @dragging="handleDragging"
      @dropped="handleDropped"
    >
      <div
        :class="['bounding-box', { 'bounding-box--selected': selected }]"
        v-click-outside="onClickOutside"
      >
        <e :outline="true" v-if="selected" />
        <e :outline="false" />
      </div>
    </drag-it-dude>
  </div>
</template>

<script>
import DragItDude from 'vue-drag-it-dude'
import vClickOutside from 'v-click-outside'
import E from '@/components/E'

export default {
  name: 'App',
  data: () => ({
    selected: false
  }),
  directives: {
    clickOutside: vClickOutside.directive
  },
  components: {
    DragItDude,
    E
  },
  methods: {
    handleActivated() {
      this.selected = true
    },
    handleDragging() {},
    handleDropped() {},
    onClickOutside() {
      this.selected = false
    }
  }
}
</script>

<style lang="scss">
$blue: #4f80ff;

body {
  margin: 0;
}
#app {
  position: relative;
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
