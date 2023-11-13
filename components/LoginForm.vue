<template>
    <div class="login-form">
      <form @submit.prevent="submitForm">
        <label for="username">Username:</label>
        <input type="text" id="username" v-model="username" required>
  
        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required>
  
        <button type="submit" id="button-login">Login</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: '',
      };
    },
    methods: {
      submitForm() {
        // Handle form submission logic here
        console.log('Username:', this.username);
        console.log('Password:', this.password);
        // Implement authentication logic if needed
      },
    },
  };
  </script>
  
  <style scoped>
  .login-form {
    max-width: 400px;
    margin: auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  form {
    display: flex;
    flex-direction: column;
  }
  
  label {
    margin-bottom: 8px;
  }
  
  input {
    padding: 8px;
    margin-bottom: 16px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  
  button {
    padding: 10px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 3px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  </style>
  