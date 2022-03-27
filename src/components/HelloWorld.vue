<template>
  <div class="hello">
    <h1 @click="onClick">{{ msg2 }}</h1>
    <button @click="onClickButton">{{buttonLabel}}</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      msg2: "hello",
      buttonLabel: "T_T",
    }
  },
  methods:{
    onClick(){
      this.msg2 = "clicked";
    },
    onClickButton(){
      if(this.buttonLabel === 'T_T'){
        this.buttonLabel = '^o^';
        return;
      }
      this.buttonLabel = 'T_T';
    }
  }
}
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
