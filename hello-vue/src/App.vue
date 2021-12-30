<template>
  <div id="app">
    <header id="header">
    <h1>Login</h1>
    </header>

    <article id="article">

      <div id="image" >
        <img  src="https://storage.googleapis.com/cdn.nhanh.vn/store/3379/ps/20190410/zzzgst006_800x800.jpg">
      </div>
      <div id="columnInput">

        <div id="containerInput"> 
          <TextInput id="textInput" v-model="name" nameInput="UserName" placeholder="UserName" type="Email" />
          <br>
          <TextInput id="textInput" v-model="pass" nameInput="Password" placeholder="Password" type="Password"  />
          <br>
          <button v-on:click="getText(name,pass)">Login</button>
        </div>

      </div>

    </article>
    <div id="footer"> 
    <p>SDT: 12035888888</p>
    </div>
  </div>
</template>

<script>
import TextInput from './components/TextInput.vue'
export default {
  name: 'App',
  components: {
    TextInput
  },
  data(){
        return {
      label: 'Username',
      name: null,
      pass: null,
    };
  },
  methods:{
    getText(name,pass){
      alert("text: "+name + "\npass: "+pass)
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
#header{
  background-color:#2c3e50;
  color: white;
  width: auto;
}
#article{
  display: grid;
  grid-template-columns: 50% 50%;
  margin: 0;
  
}
#image{
  width: auto;
  height: auto;
  text-align: right;
}
img{
border-radius: 10%;
width: 100%;
max-width: 800px;

}
#columnInput{
  text-align: left;
  width: auto;
  
}
#containerInput{
  margin: 30% 10% 10% 10%;
}
#footer{
  background-color: gray;
  padding: 20px;
  color: white;
  width: 100%;
}
button{
height: 35px;
width: 100px;
background-color: thistle;
border-radius: 30px;
}
h2 ,h6 ,h3{
  background-color: chartreuse;
}

@media screen and (max-width: 600px) {
#containerInput{
  margin: 0;
}

}
</style>
