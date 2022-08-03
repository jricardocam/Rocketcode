<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>¿Cuál es tu Fecha de Nacimiento?</h1>
        <form action="">
            <input v-model="datosFecha.dia" type="number" name="dia" id="dia" min="1" max="31" placeholder="Día" required>
            <input v-model="datosFecha.mes" type="number" name="mes" id="mes" min="1" max="12" placeholder="Mes" required>
            <input v-model="datosFecha.año" type="number" name="año" id="año" min="1950" max="2020" placeholder="Día" required>   
        </form>
        <input type="submit" value="Enviar" class="btn" @click="procesar">
    </div>
</div>
</template>


<script>  

export default{
    name: 'Contacto',
    data(){
        return{
            datosFecha: {
                dia: '',
                mes: '',
                año: ''
            }
        }
    },
    methods: {
        procesar(){
            alert(this.datosFecha.dia + '/' + this.datosFecha.mes + '/' + this.datosFecha.año);
        }
    }
}
</script>

