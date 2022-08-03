<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>¿Cuál es tu Nombre?</h1>
        <form action="">
                <input v-model="prinombre" type="text" name="prinombre" id="prinombre" placeholder="Ingresa tu Primer Nombre" required>
                <input v-model="segnombre" type="text" name="segnombre" id="segnombre" placeholder="Ingresa tu Segundo Nombre" required>
                <input v-model="appaterno" type="text" name="appaterno" id="appaterno" placeholder="Ingresa tu Apellido Paterno" required>
                <input v-model="appmaterno" type="text" name="apmaterno" id="apmaterno" placeholder="Ingresa tu Apellido Materno" required>
        </form>   
		<input type="submit" value="Enviar" class="btn" @click="procesar">
    </div>
      <div class="space">
        <div class="bub" v-for:="item of nombreCompleto">{{item.nombre}}</div>
      </div>
</div>

</template>

<script>  

export default{
    name: 'Nombre',
    data(){
        return{
            prinombre: '',
            segnombre: '',
            appaterno: '',
            appmaterno: '',
            nombreCompleto: []
        }
},
methods: {
    procesar(){
        this.nombreCompleto.push({
            nombre: this.prinombre + ' ' + this.segnombre + ' ' + this.appaterno + ' ' + this.appmaterno
            });
        this.prinombre='';
        this.segnombre='';
        this.appaterno='';
        this.appmaterno='';
        localStorage.setItem('nombreCompleto', JSON.stringify(this.nombreCompleto));
    },
created: function(){
    let datosDB= JSON.parse(localStorage.getItem('nombreCompleto'));
    if(datosDB==null){
        this.nombreCompleto=[];
    }else{
        this.nombreCompleto=datosDB;
    }
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