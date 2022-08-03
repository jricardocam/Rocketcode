<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>¿Cuál es tu Nombre?</h1>
        <form action="">
                <input v-model="datosNombre.prinombre" type="text" name="prinombre" id="prinombre" placeholder="Ingresa tu Primer Nombre" required>
                <input v-model="datosNombre.segnombre" type="text" name="segnombre" id="segnombre" placeholder="Ingresa tu Segundo Nombre" required>
                <input v-model="datosNombre.appaterno" type="text" name="appaterno" id="appaterno" placeholder="Ingresa tu Apellido Paterno" required>
                <input v-model="datosNombre.apmaterno" type="text" name="apmaterno" id="apmaterno" placeholder="Ingresa tu Apellido Materno" required>
        </form>   
		<input type="submit" value="Enviar" class="btn" @click="procesar">
    </div>
</div>
</template>

<script>  

export default{
    name: 'Nombre',
    data(){
        return{
            datosNombre: {
                prinombre: '',
				segnombre: '',
				appaterno: '',
				apmaterno: ''
            }
        }
    },
    methods: {
        procesar(){
            alert(this.datosNombre.prinombre + ' ' + this.datosNombre.segnombre + ' ' + this.datosNombre.appaterno + ' ' + this.datosNombre.apmaterno);
        }
    }
}
</script>

<style>

form{
    margin: 0px;
    padding-left: 0px;
	width: 350px;
	position: relative;	
}

input{
	width: 17em;	
	border: none;
	border-radius: 10px;
	padding: 10px;
	font-size: 1.1em;
	color: #676767;
    margin-top: 0.5em;
	
}


textarea{
	height: 100px;	
	resize: none; 
	overflow: auto;
}
.btn{
	background-color: #fc3ad5;
    border: none;
    border-radius: 10px;
	color: white;
	height: 2em;
    width: 5em;
	cursor: pointer;
	margin-top: 30px;
	font-size: 1.29em;
	-webkit-transition: background-color 0.5s;
	-moz-transition: background-color 0.5s;
	-o-transition: background-color 0.5s;
	transition: background-color 0.5s;
}
.btn:hover{
	background-color: #cc01a4;
	
}
</style>