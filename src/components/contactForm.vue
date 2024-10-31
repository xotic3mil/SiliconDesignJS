<script setup>
import { ref } from 'vue'

const fullName = ref('')
const email = ref('')
const specialist = ref('')
const errors = ref({
  fullName: '',
  email: '',
  specialist: '',
})

const validateForm = () => {
  let isValid = true
  errors.value = {
    fullName: '',
    email: '',
    specialist: '',
  }

  // Full Name validation: must not be empty and only letters/spaces allowed
  const nameRegex = /^[A-Za-z\s]+$/
  if (!fullName.value.trim()) {
    errors.value.fullName = 'Full Name is required'
    isValid = false
  } else if (!nameRegex.test(fullName.value)) {
    errors.value.fullName = 'Full Name can only contain letters and spaces'
    isValid = false
  }

  // Email validation
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  if (!email.value.trim()) {
    errors.value.email = 'Email Address is required'
    isValid = false
  } else if (!emailRegex.test(email.value)) {
    errors.value.email = 'Please enter a valid email address'
    isValid = false
  }

  // Specialist validation: must not be empty and only letters/spaces allowed
  if (!specialist.value.trim()) {
    errors.value.specialist = 'Specialist is required'
    isValid = false
  } else if (!nameRegex.test(specialist.value)) {
    errors.value.specialist = 'Specialist can only contain letters and spaces'
    isValid = false
  }

  return isValid
}

const handleSubmit = e => {
  e.preventDefault()
  if (validateForm()) {
    const user = {
      fullName: fullName.value,
      email: email.value,
      specialist: specialist.value,
    }
    console.log('Form Submitted:', user)
  }
}
</script>

<template>
  <form @submit="handleSubmit" class="reg-form">
    <h2 class="form-title">Get Online Consultation</h2>

    <div class="input-group">
      <label for="fullName" class="form-label">Full Name</label>
      <input
        v-model="fullName"
        id="fullName"
        type="text"
        required
        placeholder="Enter your full name"
        class="form-input"
        :class="{ error: errors.firstName }"
      />
      <p v-if="errors.firstName" class="invalid-input">
        {{ errors.firstName }}
      </p>
    </div>

    <div class="input-group">
      <label for="email" class="form-label">Email Address</label>
      <input
        v-model="email"
        id="email"
        type="email"
        required
        placeholder="Enter your email address"
        class="form-input"
        :class="{ error: errors.email }"
      />
      <p v-if="errors.email" class="invalid-input">{{ errors.email }}</p>
    </div>

    <div class="input-group">
      <label for="specialist" class="form-label">Specialist</label>
      <input
        v-model="specialist"
        id="specialist"
        type="text"
        required
        placeholder="Enter specialist name"
        class="form-input"
        :class="{ error: errors.specialist }"
      />
      <p v-if="errors.specialist" class="invalid-input form-input.error">
        {{ errors.specialist }}
      </p>
    </div>

    <button type="submit" class="btn-primary">Make an Appointment</button>
  </form>
</template>

<style scoped>
.reg-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 90%;
  max-width: 400px;
  margin: 0 auto;
  background: #fff;
  border-radius: 10px;
  box-shadow:
    0px 4.8px 24.4px -6px rgba(19, 16, 34, 0.1),
    0px 4px 13px -2px rgba(19, 16, 34, 0.06);
  padding: 20px;
  gap: 24px;
}

.form-title {
  font-size: 24px;
  font-weight: 800;
  text-align: center;
}

.input-group {
  display: flex;
  flex-direction: column;
  width: 100%;
  gap: 8px;
}

.form-label {
  font-weight: 600;
  line-height: 1.6;
}

.form-input {
  height: 48px;
  border: 1px solid var(--Gray-200);
  border-radius: 8px;
  padding: 0 12px;
  font-size: 16px;
}

.form-input.error {
  border-color: firebrick;
}

.invalid-input {
  color: firebrick;
  font-size: 14px;
  display: none;
}

.btn-primary {
  background: #1d4ed8; /* Brand-Primary */
  color: #fff;
  width: 100%;
  padding: 13px;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
}

.btn-primary:hover {
  background: #2563eb;
}

@media (min-width: 768px) {
  .reg-form {
    max-width: 730px;
    padding: 30px;
    gap: 32px;
  }

  .form-title {
    font-size: 28px;
  }

  .form-input {
    font-size: 18px;
  }

  .btn-primary {
    font-size: 18px;
    padding: 15px;
  }
}

/* Desktop Styles (min-width: 1400px) */

@media (min-width: 1400px) {
  .reg-form {
    padding: 40px;
    gap: 40px;
    height: 777px;
  }

  .form-title {
    font-size: 32px;
  }

  .form-input {
    font-size: 20px;
  }

  .btn-primary {
    font-size: 20px;
    width: 492px;
    padding: 13px 32px;
    gap: 8px;
    margin-top: 8rem;
  }

  .form-input.error {
    border-color: firebrick;
  }

  .invalid-input {
    color: firebrick;
    font-size: 14px;
    display: none;
  }
}
</style>
