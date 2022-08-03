<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>Contacto</h1>
        <form @submit="sendMessage">
                <input v-model="telefono" type="tel" name="telefon" id="telefono" placeholder="Ingresa tu Telefono" pattern="\([0-9]{3}\) [0-9]{3}[ -][0-9]{4}" required>
                <input v-model="email" type="email" name="email" id="email" placeholder="Ingresa tu Email" required>
        </form>
        <button class="btn" @click="SendMessage" type="submit">Enviar</button>
    </div>
</div>
    
</template>

<script>

export default{
    data(){
        return{
            email:'',
            emails:[],
            telefono:'',
        	telefonos:[]        
        }
    },
    methods : {
         sendMessage(event){
            event.preventDefault();

        const contactoInfo = {
            'email':this.email,
            'telefono':this.telefono
        }
    }
    }
}
</script>

<style>

.space{
    margin-top: 50px;
    margin-bottom: 50px;
    margin-left: 22rem;
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