<template>
  <div class="background-image">
    <img src="./assets/cat-background.jpg" alt="Cat Background" />
  </div>
  <div class="home">
    <q-banner class="banner" color="primary" icon="pets">
      <div class="banner-content">
        <h1>Welcome to our Pet Care Center</h1>
        <p>At our center, we provide the best care for your furry friends</p>
      </div>
    </q-banner>

    <div class="services">
      <h2>Our Services</h2>
      <div class="service-item">
        <q-card class="card">
          <q-card-section class="card-section">
            <q-icon name="pets" size="2em" />
            <h3>Grooming</h3>
            <p>
              We offer professional grooming services to keep your pets looking
              their best
            </p>
          </q-card-section>
        </q-card>
      </div>
      <div class="service-item">
        <q-card class="card">
          <q-card-section class="card-section">
            <q-icon name="local_hospital" size="2em" />
            <h3>Veterinary Care</h3>
            <p>
              Our on-site veterinarians are always available to provide medical
              care and advice
            </p>
          </q-card-section>
        </q-card>
      </div>
      <div class="service-item">
        <q-card class="card">
          <q-card-section class="card-section">
            <q-icon name="paw" size="2em" />
            <h3>Pet Sitting</h3>
            <p>
              Going away? Leave your pets with us and we'll make sure they're
              happy and comfortable
            </p>
          </q-card-section>
        </q-card>
      </div>
    </div>

    <div class="cta">
      <q-btn
        color="primary"
        size="lg"
        class="btn"
        @click="showContactForm = true"
        >Contact Us</q-btn
      >
      <q-dialog v-model="showContactForm">
        <q-card>
          <q-card-section>
            <h3>Contact Us</h3>
          </q-card-section>
          <q-card-section>
            <q-form @submit.prevent="submitForm">
              <q-input label="Name" v-model="form.name" required />
              <q-input label="Email" v-model="form.email" required />
              <q-textarea label="Message" v-model="form.message" required />
              <q-btn type="submit" label="Send" color="primary" />
            </q-form>
          </q-card-section>
        </q-card>
      </q-dialog>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Home',
  setup() {
    const showContactForm = ref(false);
    const form = ref({
      name: '',
      email: '',
      message: '',
    });

    function submitForm() {
      // submit form logic here
    }

    return {
      showContactForm,
      form,
      submitForm,
    };
  },
};
</script>

<style>
.banner {
  padding: 50px;
  text-align: center;
  color: white;
}

.banner-content {
  max-width: 800px;
  margin: 0 auto;
}

.services {
  margin: 50px auto;
  max-width: 800px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}

.service-item {
  display: flex;
}
</style>
