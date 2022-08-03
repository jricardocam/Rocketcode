<template>

  <div  class="home">
    <Nombre/>
    <Fecha/>
    <Contacto/>
    <div class="space">
        <input type="submit" value="Inicio" class="btn" @click="mostrar" >
          <div class="space">
          <div class="bub" v-for:="item of datosGenerales">{{item.generales}}
          <div v-for:="items of generales">{{items}}</div>
          </div>
          </div>
    </div>
  </div>

</template>

<script>
import Nombre from '../components/Nombre.vue'
import Fecha from '../components/Fecha.vue'
import Contacto from '../components/Contacto.vue'

export default {
  name: 'HomeView',
  components: {
    Nombre,
    Fecha,
    Contacto
  },
  data(){
        return{
            datosGenerales: []
        }
},
methods: {
    mostrar(){
        this.datosGenerales.push({
            generales: "Nombre Completo: "+localStorage.getItem('nombreCompleto')+
            "\nDatos de Contacto"+localStorage.getItem('datosContacto')
            +"\nFecha De Nacimiento"+localStorage.getItem('fechaCompleta')
            });
    }
}
}
</script>
<style>
body {
    background-color: #ffbff2;
}
h1{
    font-size: 1.7em;
    font-weight: bold;
    color: #000;
}
.home{
    margin: 50px 50px 50px 50px;
}

.bub {
  position: relative;
  font-family: sans-serif;
  font-size: 1.2em;
  line-height: 24px;
  width:22rem;
  background: rgb(253, 34, 144);
  border-radius: 40px;
  padding: 24px;
  text-align: center;
  color: white;
  font-weight: bold;
}

.bub:before {
  content: "";
  width: 0px;
  height: 0px;
  position: absolute;
  border-left: 12px solid transparent ;
  border-right: 24px solid rgb(253, 34, 144);
  border-top: 12px solid rgb(253, 34, 144);
  border-bottom: 20px solid transparent;
  right: 32px;
  bottom: -24px;
}
</style>