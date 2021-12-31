<template>
  <div id="app">
    <article id="article">
        <div id="containerInput"> 
          <h1>Login </h1>
          <br/>
          <TextInput id="textInput" v-model="name" nameInput="UserName" placeholder="UserName" type="email" />
          <br>
          <PasswordInput id="textInput" v-model="pass" nameInput="Password" placeholder="Password" type="password"/>
          <br>
          <button @click="getText(name,pass)">Login</button>

          <!-- <button v-on:click="handleClick($event)">click</button> -->
        </div>
    </article>
  </div>
</template>
<script>
import TextInput from './components/TextInput.vue'
import PasswordInput from './components/TextPassword.vue'
export default {
  name: 'App',
  components: {
    TextInput,
    PasswordInput
  },
  data(){
      return {
      label: 'Username',
      name: null,
      pass: null,
      src: "https://storage.googleapis.com/cdn.nhanh.vn/store/3379/ps/20190410/zzzgst006_800x800.jpg",
      number: 100000,
    };
  },
  methods:{
    getText(name,pass){
      alert("text: "+name + "\npass: "+pass)
    },
    money(){
      var numbers = this.number
      return new Intl.NumberFormat('de-DE', { style: 'currency', currency: 'VND' }).format(numbers)
    },
    handleClick(e){
        console.log("click"+e.target);
    }
  }
}
</script>

<style>
* { 
margin: 0 ;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}
#article{
background-color: turquoise;
display: flex;
justify-content: center;
align-items: center;
padding: 0 10px 0 10px;
height: 760px;
overflow:auto; 
}
#containerInput{
  background-color: white;
  padding: 40px 10px 40px 10px;
  border-radius: 20px;
  width: 100%;
  max-width: 600px;

}
button{
height: 35px;
width: 100px;
background-color: turquoise;
border-radius: 10px;
border: none;
outline:none;
}
</style>
