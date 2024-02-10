<script>
export default{
  name: 'App',

  data(){
    return{
      
      // email: '',

      emails: []
    }
  },

  created(){

    // axios
    // .get('https://flynn.boolean.careers/exercises/api/random/mail')
    // .then((response) => {
    //   console.log(response);
    //   this.email = response.data.response
    // })

    for (let i = 0; i < 10; i++) {

      axios
      .get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then((response) => {
      console.log(response);
      this.emails.push(response.data.response)
    })

    }
    
  }

}





</script>

<template>

  <!-- <div>{{ email }}</div> -->

  <div v-for="email in emails">

    {{ email }}

  </div>


</template>

<style scoped>
</style>
