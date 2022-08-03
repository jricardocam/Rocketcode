<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>¿Cuál es tu Fecha de Nacimiento?</h1>
        <form action="">
            <input v-model="dia" type="number" name="dia" id="dia" min="1" max="31" placeholder="Día" required>
            <input v-model="mes" type="number" name="mes" id="mes" min="1" max="12" placeholder="Mes" required>
            <input v-model="año" type="number" name="año" id="año" min="1950" max="2020" placeholder="Día" required>   
        </form>
        <input type="submit" value="Enviar" class="btn" @click="procesar">
    </div>
    <div class="space">
        <div class="bub" v-for="item of fechaCompleta">{{item.fecha}}</div>
      </div>
</div>
</template>


<script>  
export default{
    name: 'Contacto',
    data(){
        return{
                dia: '',
                mes: '',
                año: '',
                fechaCompleta:[]
            }
}, 
 methods: {
            procesar(){
            this.fechaCompleta.push({
                fecha: this.dia+'/'+this.mes+'/'+this.año
                });
        }
    }
}
</script>

