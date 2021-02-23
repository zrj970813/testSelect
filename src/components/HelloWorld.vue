<template>
  <div class="block">
    <el-select v-model="value" placeholder="请选择">
      <el-option
        v-for="item in options"
        :key="item.value"
        :label="item.label"
        :value="item.value">
      </el-option>
    </el-select>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      value: '',
      options: [
        { label: "长沙芙蓉区网点", value: "长沙芙蓉区网点", id: 15 },
        { label: "长沙岳麓区网点", value: "长沙岳麓区网点", id: 16 },
        { label: "长沙分拨中心", value: "长沙分拨中心", id: 17 },
        { label: "朝阳区网点", value: "朝阳区网点", id: 18 },
        { label: "海淀区网点", value: "海淀区网点", id: 19 },
        { label: "昌平区网点", value: "昌平区网点", id: 20 },
        { label: "北京分拨中心", value: "北京分拨中心", id: 21 },
        { label: "南京玄武区网点", value: "南京玄武区网点", id: 22 },
        { label: "湖北网点", value: "湖北网点", id: 32 },
        { label: "南京江宁区网点", value: "南京江宁区网点", id: 233 },
        { label: "上海黄埔网点", value: "上海黄埔网点", id: 248 }
      ]
    };
  }
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
