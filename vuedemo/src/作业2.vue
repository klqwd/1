<template>
  <div>
    <ul>
      <li v-for="(item,index) in msg" :key="item">
        {{ item }}
        <button @click='del(index)'>删除</button>
      </li>
    </ul>
    <button @click="add">生成</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: [1, 3, 4],
    };
  },
  methods: {
   
    add() {
      this.msg.push(Math.floor(Math.random()*100))
    },
    del(index){
      this.msg.splice(index,1)
    }
  },
};
</script>

<style></style>
