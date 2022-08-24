<template>
  <div>
    <ul>
      <li v-for="item in msg" :key="item">{{ item }}</li>
    </ul>
    <button @click='one'>走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: ["帅哥", "美女", "程序员"],
    };
  },
  methods: {
    one(){
      this.msg.push(this.msg[0])
      this.msg.splice(0,1)
    }
  },
};
</script>

<style></style>