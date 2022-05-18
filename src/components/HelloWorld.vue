<template>
  <div class="hello">
    <div>
      {{num}}
      <br>
      {{fullname}}
      <button @click="num++">+</button>
      <button @click="change">点击改变</button>
      <!-- <button @click="">点击改变</button> -->
    </div>
  </div>
</template>

<script>

export default {
  name: "HelloWorld",
  props: {
    
  },
  data(){
    return{
      num:0,
      first:"li",
      last:"xinying"
    }
  },
  computed:{
    fullname:{
      get(){
        return this.first + " " + this.last
      },
      set(value){
        var arr = value.split(" ");
        this.first=arr[0];
        this.last=arr[1];
      }
      
    }
  },
  methods:{
    change(){
      this.fullname="2021 7/17"
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
