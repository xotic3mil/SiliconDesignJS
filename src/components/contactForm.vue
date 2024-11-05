<script setup>
import { ref } from 'vue'

const submitted = ref(false)

const submitHandler = async formData => {
  console.log(formData)
  try {
    const response = await fetch(
      'https://win24-assignment.azurewebsites.net/api/forms/contact',
      {
        method: 'POST', 
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify(formData),
      },
    )

    console.log(response)
    if (response.ok) {
      submitted.value = true
    }
  } catch (error) {
    console.error('Error:', error)
  }
}
</script>

<template>
  <div class="reg-form">
    <FormKit
      type="form"
      id="registration"
      :form-class="submitted ? 'hide' : 'show'"
      submit-label="Register"
      @submit="submitHandler"
      :actions="false"
      #default="{ value }"
    >
      <h1>Get Online Consultation</h1>

      <FormKit
        type="text"
        name="fullName"
        label="Full Name"
        placeholder="Jane Doe"
        help="What do people call you?"
        validation="required"
      />

      <FormKit
        type="text"
        name="email"
        label="Your email"
        placeholder="jane@example.com"
        help="What email should we use?"
        validation="required|email:/^[^@\s]+@[^@\s]+\.[^@\s]+$"
      />

      <FormKit
        type="select"
        name="Specialist"
        label="Specialist"
        placeholder="Select specialization"
        help="Medical Specialties and Subspecialties"
        :options="[
          'Allergy and Immunology',
          'Anesthesiology',
          'Cardiology',
          'Colon and Rectal Surgery',
          'Neurology',
          'Ophthalmic Surgery',
          'Orthopaedic Surgery',
          'Pediatrics',
          'Preventive Medicine',
          'Radiology',
          'Urology',
          'Emergency Medicine',
        ]"
      />

      <FormKit type="submit" class="btn-primary" label="Make an Appointment" />
    </FormKit>

    <div v-if="submitted">
      <h2>Submission successful!</h2>
    </div>
  </div>
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

.super-red {
  color: red;
}

.input-group {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  gap: 8px;
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
    width: 500px;
  }

  .btn-primary {
    font-size: 20px;
    width: 492px;
    padding: 13px 32px;
    gap: 8px;
    margin-top: 8rem;
  }

  .input-group {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    gap: 20px;
  }
}
</style>
