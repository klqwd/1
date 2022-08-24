<template>
  <div id='app'>
    <table class='tb'>
      <tr>
        <th v-for='item in msg' :key='item'>{{item}}</th>
      </tr>
      <tr v-for='(obj,index) in val' :key='obj'>
        <td>{{obj.id}}</td>
        <td>{{obj.name}}</td>
        <td>{{obj.time}}</td>
        <td><button @click='del(index)'>{{obj.handle}}</button></td>
      </tr>

      <tr v-if='val.length===0'>
        <td colspan="4">没有数据咯~</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data(){
    return{
      msg:['编号','品牌名称','创立事件','操作'],
      val:
      [{id:1,name:'奔驰',time:'2020-08-01',handle:'删除'},
      {id:2,name:'宝马',time:'2020-08-02',handle:'删除'},
      {id:3,name:'奥迪',time:'2020-08-03',handle:'删除'}]
    }
  },
  methods: {
    del(index){
      this.val.splice(index,1)
    }
  },
}
</script>

<style>
#app {
  width: 600px;
  margin: 10px auto;
}

.tb {
  border-collapse: collapse;
  width: 100%;
}

.tb th {
  background-color: #0094ff;
  color: white;
}

.tb td,
.tb th {
  padding: 5px;
  border: 1px solid black;
  text-align: center;
}

.add {
  padding: 5px;
  border: 1px solid black;
  margin-bottom: 10px;
}
</style>