<template>
  <div>

 
  <form action="" class="myform" method="POST">

      <div class="form-group">
        <label for="user_role"> Property </label> <br>
        <select name="destination" class="custom-select" v-model="location" required>
          <option>Select Destination</option>
          <option>Bishoftu</option>
          <option>Adama</option>
          <option>Entoto</option>
          <option>Lake Tana</option>
          <option>Awash</option>
          <option>Boston</option>
        </select>
      </div>

      <input type="date" v-model="checkIn" />


      <input type="date" v-model="checkOut" />


      <input type="submit" @submit="getData" value="book now">
    </form>

     <div v-for="row in data" :key="row">
        <p>{{ row }}</p>
     </div>
     </div>
</template>

<script>
export default {

  data(){
    return {
      checkIn: '',
      checkOut: '',
      location: '',
      data:''
    }
  },
  methods: {
    getData(){
      axios.post('http://localhost/reservation_system/book.php',{
        action: 'fetchall'
      }).then(response => {
        this.data = response.data
      })
    },
  }
}
</script>

<style lang="scss" scoped>
.myform{
  margin-top: 2rem;
}
</style>