<template>
  <div class="select-main">
    <input 
    type="text" 
    class="select-main_input"
    @focus.self="focus" 
    @click.stop="() => {}"
   
    readonly 
    :value="value"/>
    <div class="select-main_wrap" v-show="show">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    value: [String, Number, Boolean],
  },
  provide () {
    return {
      options: this,
    }
  },
  watch: {
    show(val) {
      if (val) {
        window.addEventListener('click', this.callback, false)
      } else {
        window.removeEventListener('click', this.callback)
      }
    }
  },
  data() {
    return {
      show:false
    }
  },
  methods: {
    callback() {
      this.show = false
    },
    focus() {
      this.show = true
    },
    getData (options) {
      this.$emit('input', options.value)
      this.show = false
    },
  },
}
</script>

<style lang="scss">
  .select-main {
    position: relative;
    display: inline-block;
    .select-main_input {
      cursor: pointer;
      height: 20px;
    }
    .select-main_wrap {
      position: absolute;
      background: #fff;
      border: 1px solid #000;
      left: 0;
      right: 0;
      top: 30px;
    }
  }
</style>