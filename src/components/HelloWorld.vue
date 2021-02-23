<template>
  <div class="block">
    <eselect v-model="a1">
      <eselectitem 
      :value="item.value" 
      :label="item.label" 
      v-for="(item, index) in a1List" 
      :key="index"></eselectitem>
    </eselect>
   
  </div>
</template>

<script>
import eselect from './select/main'
import eselectitem from './select/mian-item'
export default {
  name: "HelloWorld",
  components: {
    eselect,
    eselectitem
  },
  data() {
    return {
      value: '',
      a1: '',
      a1List: [{
        label: 1,
        value: 1
      }, {
        label: 2,
        value: 2
      }],

      
    };
  },
  watch: {
    a1() {
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
