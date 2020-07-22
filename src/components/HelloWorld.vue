<template>
  <div class="wrap">
    <img :src="require(`../assets/${name}.jpg`)" alt="">
    <div class="container">
      <input @click="showZoe" class="botons" type="submit" value="zoe">
      <input @click="showNeeko" class="botons" type="submit" value="neeko">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      name: "zoe"
    }
  },
  methods: {
    showZoe(){
      this.name = "zoe"
    },
    showNeeko(){
      this.name = "neeko"
    }
  },
  beforeUpdate(){
    alert(`Haz cambiado a ${this.name == "zoe" ? "zoe" : "neeko"}`)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .wrap {
    width: 1200px;
    background: #24303c;
    padding: 30px;
    margin: auto;
    margin-top: 100px;
    border-radius: 4px;
    font-family: 'calibri';
    color: white;
    box-shadow: 7px 13px 37px #000;
  }
  .botons {
    width: 40%;
    background: #1f53c5;
    border: none;
    padding: 12px;
    color: white;
    margin: 16px 16px;
    font-size: 16px;
    }

  .botons:hover {
    background: green;
    border: 1px solid white;
    } 

</style>
