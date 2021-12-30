<template>
  <div id="textInput">
    <form>
    <label for="fname">{{ nameInput }}</label><br>
    <input v-model="username" :placeholder="placeholder" :type="type" >
    </form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    nameInput: String,
    placeholder : String,
    type: String
  },
  // data(){
  //   return{
  //     type:"password"
  //   }
  // },
  computed:{
    username:{
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
  width: 100%;
  text-align: center;
  
}
label{
  margin-left: 10px;
}
input{
  width: 100%;
  max-width: 400px;
  height: 30px;
  padding-left: 10px;
  outline: none;
  border-radius: 30px;
}
form{
  text-align: left;
}
</style>
