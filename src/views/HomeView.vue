<template>
  <div class="home">
    <Nombre/>
    <Fecha/>
    <Contacto/>
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
  }
}
</script>
