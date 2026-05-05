<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      App para um contador apartir do zero
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <p class="numero">{{ numero }}</p>
      <button @click="adicionar" class="btn"> Adicionar </button>  
    </ul>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  shame:'CaixaNumero',
  data() {
    return{
      numero: 0
    }
  },
  methods: {
    adicionar(){
      this.numero++
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
.caixa-numero {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  font-family: Arial, sans-serif;
}

.caixa {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 15px;
  padding: 40px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  color: white;
}

.numero {
  font-size: 36px;
  font-weight: bold;
  margin: 20px 0;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
}

h3 {
  margin: 0 0 15px 0;
  font-size: 24px;
}

button {
  background: rgba(255,255,255,0.2);
  border: 2px solid black;
  color: black;
  padding: 10px 20px;
  margin-top: 20px;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
  transition: background 0.3s;
}

button:hover {
  background: rgba(255,255,255,0.3);
}

.btn{
  align-self: auto;
}
</style>
