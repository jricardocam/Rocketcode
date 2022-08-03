<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>Contacto</h1>
        <form >
                <input v-model="telefono" type="tel" name="telefon" id="telefono" placeholder="Ingresa tu Telefono" pattern="\([0-9]{3}\) [0-9]{3}[ -][0-9]{4}" required>
                <input v-model="email" type="email" name="email" id="email" placeholder="Ingresa tu Email" required>
        </form>
        <input type="submit" value="Enviar" class="btn" @click="procesar" >
    </div>
    <div class="space">
        <div class="bub" v-for:="item of datosContacto">{{item.contacto}}</div>
      </div>
</div>
</template>

<script>  
export default{
    name: 'Contacto',
    data(){
        return{
                telefono: '',
                email: '',
                datosContacto:[]
            }
}, 
 methods: {
            procesar(){
            this.datosContacto.push({
                contacto: this.telefono+'\n'+this.email
                });
            this.telefono='';
            this.email='';
            localStorage.setItem('datosContacto', JSON.stringify(this.datosContacto));
            }
        },
created: function(){
    let datosDB= JSON.parse(localStorage.getItem('datosContacto'));
    if(datosDB==null){
        this.datosContacto=[];
    }else{
        this.datosContacto=datosDB;
    }
}

}
</script>

<style>

.space{
    margin-top: 50px;
    margin-bottom: 50px;
    margin-left: 15.5rem;
}

.bubble {
  position: relative;
  font-family: sans-serif;
  font-size: 16px;
  line-height: 24px;
  width:22rem;
  background: #f1ebee;
  border-radius: 40px;
  padding: 24px;
  text-align: center;
  color: #000;
}

.bubble-bottom-left:before {
  content: "";
  width: 0px;
  height: 0px;
  position: absolute;
  border-left: 24px solid #f1ebee;
  border-right: 12px solid transparent;
  border-top: 12px solid #f1ebee;
  border-bottom: 20px solid transparent;
  left: 32px;
  bottom: -24px;
}

</style>