<template>
  <div id="textInput">
    <div id="container">
      <label for="fname">{{ nameInput }}</label><br>
      <div id="styleInput">
        <input v-model="passs" :placeholder="placeholder" :type="type"  >
        <div id="check">
          <p  v-on:click="type==='password'? type='text':type='password'">{{type=="password"? "o.o":"-.-"}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'textPassword',
  props: {
    nameInput: String,
    placeholder : String,
    },
  data(){
    return{
       type :"password",
    }
  },
  methods:{
  },
  computed:{
    passs:{
      get() {
        return this.value;
      },
      set(val) {
        this.$emit("input", val);
      },
    },
  },
}
</script>
<style scoped>
#textInput{
  height: auto;
  width:100% ;

  display: flex;
  align-items: center;
  justify-content: center;
}
#container{
  width: 100%;
  max-width:300px ;
  height: auto;
  text-align: left;
}
#styleInput{
  border: 0.1px outset gray;
  display: grid;
  grid-template-columns: 90% 10%;
  background-color: turquoise;
}
#check{
  
  display: flex;
  align-items: center;
  justify-content: center;
}
input{
  height: 30px;
  display:block;
  border: none;
  outline:none;
}
</style>
