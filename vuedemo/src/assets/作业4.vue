<template>
  <div>
    <table>
      <tr>
      苹果10 ￥/斤，折扣 <8折>
      </tr>
      <tr>请输入你要购买的斤数
        <input type="text" v-model='num'>
      </tr>
      <tr><button @click='one'>结账买单</button></tr>

      <tr>结账单：总价{{num1}}元 折后价{{Math.floor(num1*80)/100}}元 省了：{{Math.floor(num1*20)/100}}元</tr>

    </table>
  </div>
</template>

<script>
export default {
  data(){
    return{
      num:'0',
      num1:'0'
    }
  },
  methods: {
    one(){
      this.num1=this.num
    }
  },
};
</script>

<style></style>
