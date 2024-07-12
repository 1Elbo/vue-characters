<template>
  <h1>Characters</h1>
  <h2 v-if="chars.length===0">No characters added yet</h2>
  <ul>
    <li v-for="(char, index) in chars" :key="index">
      {{ char }}
      <div class="cross" @click="removeCharacter">
        <div class="bar1"></div>
        <div class="bar2"></div>
      </div>
    </li>
    <button class="delete" v-if="chars.length != 0" @click="deleteAll">Delete all</button>
    
  </ul>
  <form @submit.prevent="chars.push(newChar)">
    <input type="text" placeholder="Add character here" v-model="newChar"/><br>
    <button class="button-30" role="button" >Add Character</button>
  </form>
  
</template>

<script>
  export default {
    data() {
      return {
        newChar: "",
        chars: ["sdsd"]
      }
    },
    methods: {
      /* addNewCharacter(){
        this.chars = this.chars.push(this.newChar);
      } */
     removeCharacter(index){
      this.chars.splice(index, 1);
     },
     deleteAll(){
      this.chars = [];
     }
    }
  }
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
*:focus{
  outline: none;
}
/* .delete{
  
} */
body{
  background-color: rgb(46, 27, 82);
  display: flex;
  justify-content: center;
}
h1{
  font-size: 4rem;
  padding-top: 30px;
  text-align: center;
}
h2{
  text-align: center;
  color: red;
  font-weight: 200;
}
ul{
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 400px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
li{
  font-size: 2rem;
  text-align: center;
  padding-block: 20px;
  margin-top: 20px;
  background-color: #bada55;
  position: relative;
  width: 100%
  
}
.cross{
  border-radius: 50%;
  flex-direction: column;
  width: 26px;
  height: 26px;
  
  position: absolute;
  right: 10px;
  top: 50%;
  transform: translateY(-13px);
}
.cross:hover{
  cursor: pointer;
}
.bar1,
.bar2{
  
  top: 50%;
  position: absolute;
  width: 100%;
  height: 2px;
  background-color: red;
  transform: translateY(-1px);
  border-radius: 50px;
}
.bar1{
  transform: rotate(-45deg);
}
.bar2{
  transform: rotate(45deg);
}
input{
  background-color: rgb(46, 27, 82);
  border: none;
  border-bottom: 2px solid white;
  padding-top: 10px;
  margin-top: 50px;
  width: 400px;
  color: white;
  font-size: 1.5rem;
}

form{
  display: flex;
  flex-direction: column;
  align-items: center;
}
button{
  padding-inline: 20px;
  padding-block: 10px;
  width: 50%;
  background-color: transparent;
  text-transform: uppercase;
  color:white;
  border: 0;
}
button:hover{
  cursor: pointer;
  
}



/* CSS */
.button-30 {
  align-items: center;
  appearance: none;
  background-color: #FCFCFD;
  border-radius: 4px;
  border-width: 0;
  box-shadow: rgba(45, 35, 66, 0.4) 0 2px 4px,rgba(45, 35, 66, 0.3) 0 7px 13px -3px,#D6D6E7 0 -3px 0 inset;
  box-sizing: border-box;
  color: #36395A;
  cursor: pointer;
  display: inline-flex;
  font-family: "JetBrains Mono",monospace;
  height: 48px;
  justify-content: center;
  line-height: 1;
  list-style: none;
  overflow: hidden;
  padding-left: 16px;
  padding-right: 16px;
  position: relative;
  text-align: left;
  text-decoration: none;
  transition: box-shadow .15s,transform .15s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  will-change: box-shadow,transform;
  font-size: 18px;
}

.button-30:focus {
  box-shadow: #D6D6E7 0 0 0 1.5px inset, rgba(45, 35, 66, 0.4) 0 2px 4px, rgba(45, 35, 66, 0.3) 0 7px 13px -3px, #D6D6E7 0 -3px 0 inset;
}

.button-30:hover {
  box-shadow: rgba(45, 35, 66, 0.4) 0 4px 8px, rgba(45, 35, 66, 0.3) 0 7px 13px -3px, #D6D6E7 0 -3px 0 inset;
  transform: translateY(-2px);
}

.button-30:active {
  box-shadow: #D6D6E7 0 3px 7px inset;
  transform: translateY(2px);
}
</style>