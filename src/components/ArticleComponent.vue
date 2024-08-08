<template>
<h1>{{ title }}</h1>
  <ul>
    <li v-for="name in names">
      {{name}}
    </li>
  </ul>

  <label for="email">EMAIL</label> <br>
  <input type="text" id="email" v-model="email"><br>
  <label for="password">PASSWORD</label><br>
  <input type="password" id="password" v-model="password"><br>
  <label>POSITION</label><br>
  <select v-model="select">
    <option value="frontend developer">Frontend Developer</option>
    <option value="backend developer">Backend Developer</option>
    <option value="android developer">Android Developer</option>
  </select><br>
  <label style="display: inline-block">Accept all terms and conditions</label>
  <div>
     <span>Uzbek</span><input type="checkbox" value="Uzbek" v-model="languages">
  </div>
  <div>
     <span>English</span> <input type="checkbox" value="English" v-model="languages">
  </div>
  <div>
     <span>Russian</span><input type="checkbox" value="Russian" v-model="languages">
  </div>
  <div>
   <span>Arab</span> <input type="checkbox" value="Arab" v-model="languages">
  </div>
  <div>
    <label for="skill">SKILLS</label><br>
    <input type="text" id="skill" v-model="tempSkill">
  </div>
  <form>
    <div>
      {{email}} <br>
      {{password}}<br>
      {{select}} <br>
      <ul>
        <li v-for="language in languages" :key="language">
          {{language}}
        </li>
      </ul>
      {{tempSkill}}
    </div>
  </form>
</template>

<script>
export default {
  props: ['names'],
  name: "Article",
  data(){
    return{
      title:'Article Component',
      email:'',
      password:'',
      select:'',
      languages:[],
      tempSkill:''
    }
  }
}
</script>




<style scoped>
  h1 {
    color: red;
  }
  input{
    width: 200px;
    height: 20px;
    box-shadow: 0 5px 10px #909090;
    border: none;
  }
  input:focus{
    width: 210px;
    height: 22px;
  }
  select{
    width: 200px;
    box-shadow: 0 5px 10px #909090;
    height: 20px;
    border: none;
  }
  label{
    margin-top: 30px;
  }
  select option:hover{
    background-color:#909090
  }
  p{
    font-family: sans-serif;
  }
  input[type=checkbox]{
    position: relative;
    display: inline-block;
    width: 15px;
    height: 15px;
  }
  ul li{
    list-style: none;
  }

</style>