<template>
  <div class="select-main_options" @click.stop="onSelect()">
    <slot>{{label}}</slot>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: [String, Boolean, Number],
      default: ''
    },
    value: {
      type: [String, Boolean, Number],
      default: ''
    },
  },
  inject: ['options'],
  methods: {
    onSelect () {
      this.options.getData(this)
    }
  }
}
</script>

<style lang="scss">
  .select-main_options {
    // background: ;
    padding: 10px;
    box-sizing: border-box;
    cursor: pointer;
    &:hover {
      background: #eee;
    }
  }
  .select-main_options + .select-main_options {
    border-top: 1px solid #eee;
  }
</style>