<template>
  <div>
    <TheHeader> 
      <!-- <template v-slot:title>
        Header
      </template> -->
      <template v-slot:description>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
      </template>

      Dicta provident hic, cupiditate voluptatem rem quam, nostrum, distinctio eius excepturi accusantium tempore quaerat doloremque obcaecati. Delectus doloremque tempora enim animi nam!
      
    </TheHeader>
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader.vue';


export default {
  name: 'App',
  components: { TheHeader },
  data() {
    return {
    }
  },

  watch: {
  },
  
  computed: {
  },
  
  methods: {
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
