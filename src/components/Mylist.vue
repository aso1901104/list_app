<template>
    <div>
        <h3>{{ message }}</h3>
        <div>
        <input type="text" v-model="input">
        <button v-on:click="doAction">クリック</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Mylist',
    props:{
        message: String,
    },
    data:function(){
    return {
      input:'input here.',
    };
  },
  methods:{
    doAction: function(){
      this.$emit('result-event', this.input);
    }
  }
}
</script>

<style>
div{
  margin:0px;
  padding:0px;
  text-align:center;
}
p{
  margin:0px;
  color:#666;
  font-size:16pt;
}
</style>
