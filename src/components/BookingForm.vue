<template>
  <div class="booking-form">
    <h2>Booking Form</h2>
    <form @submit.prevent="submitForm">
      <div>
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="formData.name" required />
      </div>
      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="formData.email" required />
      </div>
      <div>
        <label for="date">Date:</label>
        <input type="date" id="date" v-model="formData.date" required />
      </div>
      <div>
        <label for="time">Time:</label>
        <input type="time" id="time" v-model="formData.time" required />
      </div>
      <button type="submit">Book Now</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        date: '',
        time: ''
      }
    };
  },
  methods: {
    submitForm() {
      // Handle form submission logic here
      console.log('Form submitted:', this.formData);
    }
  }
};
</script>

<style scoped>
.booking-form {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.booking-form h2 {
  text-align: center;
}

.booking-form div {
  margin-bottom: 15px;
}

.booking-form label {
  display: block;
  margin-bottom: 5px;
}

.booking-form input {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

.booking-form button {
  width: 100%;
  padding: 10px;
  background-color: #28a745;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.booking-form button:hover {
  background-color: #218838;
}
</style>