<template>
  <div class="home">
    <h1>Welcome to the Booking Application</h1>
    <p>This is the home page of the booking application.</p>
    <BookingForm />
  </div>
</template>

<script>
import BookingForm from '../components/BookingForm.vue';

export default {
  name: 'Home',
  components: {
    BookingForm
  }
};
</script>

<style scoped>
.home {
  text-align: center;
  margin-top: 50px;
}
</style>