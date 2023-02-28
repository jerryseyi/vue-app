<script>
  export default {
    mounted() {
      console.log('mounted')
    },

    created() {
      console.log('created')
    },
    data() {
      return {
        isValid: false,
        state: 'unverified',
        counter: 0
      }
    },
    methods: {
      getStatus () {
        this.isValid = ! this.isValid;
      },

      currentState() {
        this.state = 'verified';
      },

      incrementCounter() {
        this.counter++;
      }
    }
  }
</script>

<template>
  <div>
    <button @click="getStatus">Click me</button>
    <br>
    <h1>{{ isValid }}</h1>
    <br><br>
    <button @click="currentState">Get current State</button>
    <p>The current state is {{state}}</p>
    <h3>Counter</h3>
    <p>counter is {{ counter }} <a @click.prevent="incrementCounter">increment counter</a></p>
  </div>
</template>

<style scoped>

</style>
