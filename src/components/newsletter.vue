<script setup>
import { ref } from 'vue'

const submitted = ref(false)

const submitHandler = async formData => {
  console.log(formData)
  try {
    const response = await fetch(
      'https://win24-assignment.azurewebsites.net/api/forms/subscribe',
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
  <div class="input">
    <FormKit
      type="form"
      id="registration"
      :form-class="submitted ? 'hide' : 'show'"
      submit-label="Register"
      @submit="submitHandler"
      :actions="false"
      #default="{ value }"
    >
      <FormKit
        type="text"
        name="email"
        placeholder="jane@doe.com"
        validation="email:/^[^@\s]+@[^@\s]+\.[^@\s]+$"
      />
      <FormKit type="submit" class="sub-button" label="Subscribe" />
    </FormKit>
  </div>

  <div v-if="submitted" class="submit">
    <h4>Subscribed</h4>
  </div>
</template>
<style scoped>
form {
  display: flex;
}

@media (min-width: 768px) {
  #registration {
    width: 300px;
  }
}

@media (min-width: 1400px) {
  #registration {
    min-width: 400px;
  }
}
</style>
