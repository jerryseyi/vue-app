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
        counter: 0,
        firstName: 'Negla',
        lastName: 'Abubakar'
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
    },

    computed: {
      fullname() {
        return this.firstName + ' ' + this.lastName;
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
    <input type="text" v-model="state">
    <br>
    <br>
    <br>

    <h3>welcome {{ fullname }}</h3>
  </div>
</template>

<style scoped>

</style>
