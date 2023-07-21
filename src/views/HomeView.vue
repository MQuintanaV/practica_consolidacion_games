<template>
  <div class="home">
<h1>Lita de Juegos Disponibles</h1>
<juegos></juegos>
  </div>
</template>

<script>
// @ is an alias to /src
import juegos from '@/components/juegos.vue';

export default {
  name: 'HomeView',
  components: {
    juegos
  }
}
</script>
