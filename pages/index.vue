<template>
  <div>
    <h1>HOLA {{ msg }}</h1>

    <input type="text" v-model="msg">
    <button @click="guardar"> guardar</button>

    <table>
      <tr>
        <th>nombre</th>
      </tr>
      <tr v-for="(item, index) in municipio" :key="index">
        <td>{{ item }}</td>
      </tr>
    
    </table>
  </div>
</template>
<script>
export default {
  data() {
    return { msg: "Eduar Alexi", municipio: ["mocoa", "aqui", "puerto"] 
    };
  },

  methods:{
      guardar(){
          
          this.municipio.push(this.msg)
          this.msg =" "

      }  }
};
</script>
