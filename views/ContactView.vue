<!-- <template>
    <div class="main-template">
        <div class="main-section">
        <span v-if="!sent">
        <span>
        <h1>Contact Us</h1>

        <p>If you have a quesion or an article to send us, fill out the form below and we will 
            get back to you
        </p>
        

        <form class="contact-form">       
        <p>Name<br>
        <input v-model="user_name"> </p>
        <p>Email<br>
        <input v-model="user_email"></p>
        <p>Phone<br>
        <input v-model.number="user_phone"> </p>
        <p>Question or report details<br>
        <textarea v-model="user_job" :placeholder="theJob"> enter name</textarea></p>

        <p>Upload Link</p>
        <button type="button" >Upload your report</button><br>

        <button type="button" class="job-request-btn" @click="send_request">Send!</button>
        </form>
    </span></span>
    <span v-if="sent">
        <h1>Thank You for contacting us ya legend</h1>
        <p>We will get back to you as soon as possible</p>
    </span>

    </div></div>
</template>

<script setup>

import { ref } from 'vue'

const sent = ref(false)
const user_name = ref('')
const user_email = ref('')
const user_phone = ref(null)
const user_job = ref('')


function send_request(){
    sent.value = true
}

const theJob = ref('Type as much detail about the job as required')

</script> -->

<template>
    <div class="main-heading">
        <span v-if="!sent">
        <span>
        <h1>Contact Us</h1>

        <p>If you have a quesion or an article to send us, fill out the form below and we will 
            get back to you
        </p>
        

        <form class="contact-form">       
        <p>Name<br>
        <input v-model="user_name"> </p>
        <p>Email<br>
        <input v-model="user_email"></p>
        <p>Phone<br>
        <input v-model.number="user_phone"> </p>
        <p>Question or report details<br>
        <textarea v-model="user_job" :placeholder="theJob"> enter name</textarea></p>

        <p>Upload Link</p>
        <button type="button" >Upload your report</button><br>

        <button type="button" class="job-request-btn" @click="send_request">Send!</button>
        </form>
    </span></span>
    <span v-if="sent">
        <h1>Thank You for contacting us ya legend</h1>
        <p>We will get back to you as soon as possible</p>
    </span>

    </div>

<!-- <div class="main-heading">
    <h1>Contact us</h1>
    <p>Ask a Question or upload an article for us to review and possibly
        add to our site!
    </p>
</div>

    <div class="contact-form">
      <form @submit.prevent="submitForm">
        <div class="input-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="formData.name" required />
        </div>
  
        <div class="input-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
  
        <div class="input-group">
          <label for="message">Message:</label>
          <textarea id="message" v-model="formData.message" required></textarea>
        </div>
  
        <div class="input-group">
          <label for="report">Upload Historical Report:</label>
          <input type="file" id="report" ref="fileInput" @change="handleFileUpload" />
        </div>
  
        <button type="submit">Submit</button>
      </form>
    </div> -->
  </template>
  

<script setup>

import { ref } from 'vue'

const sent = ref(false)
const user_name = ref('')
const user_email = ref('')
const user_phone = ref(null)
const user_job = ref('')


function send_request(){
    sent.value = true
}

const theJob = ref('Type as much detail about the job as required')

</script>
  <!-- <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: '',
          message: '',
          file: null
        }
      };
    },
    methods: {
      handleFileUpload() {
        this.formData.file = this.$refs.fileInput.files[0];
      },
      submitForm() {
        // TODO: Process form data, send to server or use a service like emailJS or others.
        console.log(this.formData);
        alert('Form submitted! (For demonstration purposes only. Please integrate with a backend or service.)');
      }
    }
  };
  </script>
   -->
  <style scoped>
  .contact-form {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #eee;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
  
  .input-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 10px;
  }
  
  input[type="text"],
  input[type="email"],
  textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    padding: 10px 15px;
    background-color: #333;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #555;
  }
  </style>
  