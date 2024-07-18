<template>
  <form @submit.prevent="submitForm" class="bg-white rounded-lg p-14">
    <h3 class="text-2xl font-semibold mb-6">Register for the webinar</h3>
    <div class="grid grid-cols-1 gap-3">
      <div>
        <label for="firstName" class="block text-sm mb-2">First Name*</label>
        <input
          v-model="form.firstName"
          type="text"
          id="firstName"
          required
          @input="validateField('firstName')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.firstName }"
        />
        <p v-if="errors.firstName" class="text-red-500 text-sm mt-1">
          {{ errors.firstName }}
        </p>
      </div>
      <div>
        <label for="lastName" class="block text-sm mb-2">Last Name*</label>
        <input
          v-model="form.lastName"
          type="text"
          id="lastName"
          required
          @input="validateField('lastName')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.lastName }"
        />
        <p v-if="errors.lastName" class="text-red-500 text-sm mt-1">
          {{ errors.lastName }}
        </p>
      </div>
      <div>
        <label for="workEmail" class="block text-sm mb-2">Work Email*</label>
        <input
          v-model="form.workEmail"
          type="email"
          id="workEmail"
          required
          @input="validateField('workEmail')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.workEmail }"
        />
        <p v-if="errors.workEmail" class="text-red-500 text-sm mt-1">
          {{ errors.workEmail }}
        </p>
      </div>
      <div>
        <label for="company" class="block text-sm mb-2">Company*</label>
        <input
          v-model="form.company"
          type="text"
          id="company"
          required
          @input="validateField('company')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.company }"
        />
        <p v-if="errors.company" class="text-red-500 text-sm mt-1">
          {{ errors.company }}
        </p>
      </div>
      <div>
        <label for="jobTitle" class="block text-sm mb-2">Job Title*</label>
        <input
          v-model="form.jobTitle"
          type="text"
          id="jobTitle"
          required
          @input="validateField('jobTitle')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.jobTitle }"
        />
        <p v-if="errors.jobTitle" class="text-red-500 text-sm mt-1">
          {{ errors.jobTitle }}
        </p>
      </div>
      <div>
        <label for="industry" class="block text-sm mb-2">Industry*</label>
        <select
          v-model="form.industry"
          id="industry"
          required
          @change="validateField('industry')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.industry }"
        >
          <option value="">Select an industry</option>
          <option value="Healthcare">Healthcare</option>
          <option value="Financial Services">Financial Services</option>
          <option value="Retail + eCommerce">Retail + eCommerce</option>
        </select>
        <p v-if="errors.industry" class="text-red-500 text-sm mt-1">
          {{ errors.industry }}
        </p>
      </div>
      <div>
        <label for="services" class="block text-sm mb-2">Services*</label>
        <select
          v-model="form.services"
          id="services"
          required
          @change="validateField('services')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.services }"
        >
          <option value="">Select a service</option>
          <option value="DCX">DCX</option>
          <option value="R+R">R+R</option>
          <option value="T+S">T+S</option>
          <option value="LaaS">LaaS</option>
          <option value="AI Services">AI Services</option>
        </select>
        <p v-if="errors.services" class="text-red-500 text-sm mt-1">
          {{ errors.services }}
        </p>
      </div>
      <div>
        <label for="country" class="block text-sm mb-2">Country*</label>
        <select
          v-model="form.country"
          id="country"
          required
          @change="validateField('country')"
          class="w-full px-3 py-2 border rounded"
          :class="{ 'border-red-500': errors.country }"
        >
          <option value="">Select a country</option>
          <option v-for="country in countries" :key="country.code" :value="country.code">
            {{ country.name }}
          </option>
        </select>
        <p v-if="errors.country" class="text-red-500 text-sm mt-1">
          {{ errors.country }}
        </p>
      </div>
    </div>
    <div class="mt-6">
      <label class="flex items-center">
        <input
          v-model="form.agreed"
          type="checkbox"
          required
          @change="validateField('agreed')"
          class="mr-2"
        />
        <span
          >I have read and agree to the
          <a href="#" class="text-[#065BFF] hover:underline">Privacy Policy</a>*</span
        >
      </label>
      <p v-if="errors.agreed" class="text-red-500 text-sm mt-1">{{ errors.agreed }}</p>
    </div>
    <button
      type="submit"
      class="mt-6 px-6 py-3 bg-[#065BFF] text-white rounded-full font-semibold hover:bg-blue-700"
      :disabled="!isFormValid"
    >
      Register now
    </button>
  </form>
</template>

<script setup>
import { ref, computed } from "vue";

const countries = [
  { code: "AF", name: "Afghanistan" },
  { code: "AL", name: "Albania" },
  { code: "DZ", name: "Algeria" },
  { code: "AS", name: "American Samoa" },
  { code: "AD", name: "Andorra" },
  { code: "AO", name: "Angola" },
  { code: "AI", name: "Anguilla" },
  { code: "PH", name: "Philippines" },
];

const form = ref({
  firstName: "",
  lastName: "",
  workEmail: "",
  company: "",
  jobTitle: "",
  industry: "",
  services: "",
  country: "",
  agreed: false,
});
const errors = ref({});

const isFormValid = computed(() => {
  return (
    Object.keys(form.value).every((key) => {
      if (key === "agreed") return form.value[key] === true;
      return form.value[key] !== "";
    }) && Object.keys(errors.value).every((key) => !errors.value[key])
  );
});

const validateField = (field) => {
  errors.value[field] = "";

  if (field !== "agreed" && !form.value[field]) {
    errors.value[field] = `${field.charAt(0).toUpperCase() + field.slice(1)} is required`;
    return;
  }

  switch (field) {
    case "firstName":
    case "lastName":
      if (/\d/.test(form.value[field])) {
        errors.value[field] = `${
          field === "firstName" ? "First" : "Last"
        } name should not contain numbers`;
      } else if (!/^[a-zA-Z\s'-]{2,}$/.test(form.value[field])) {
        errors.value[field] = `Please enter a valid ${
          field === "firstName" ? "first" : "last"
        } name`;
      }
      break;
    case "workEmail":
      if (!/^[\w-]+(\.[\w-]+)*@([\w-]+\.)+[a-zA-Z]{2,7}$/.test(form.value.workEmail)) {
        errors.value.workEmail = "Please enter a valid email address";
      } else {
        const domain = form.value.workEmail.split("@")[1];
        const commonPersonalDomains = [
          "gmail.com",
          "yahoo.com",
          "hotmail.com",
          "outlook.com",
          "aol.com",
        ];
        if (commonPersonalDomains.includes(domain)) {
          errors.value.workEmail = "Consider using a work email address if available";
        }
      }
      break;
    case "company":
    case "jobTitle":
      if (!/^[a-zA-Z0-9\s'-]{2,}$/.test(form.value[field])) {
        errors.value[field] = `Please enter a valid ${
          field === "company" ? "company name" : "job title"
        }`;
      }
      break;
    case "industry":
    case "services":
    case "country":
      if (!form.value[field]) {
        errors.value[field] = `Please select a ${field}`;
      }
      break;
    case "agreed":
      if (!form.value.agreed) {
        errors.value.agreed = "You must agree to the Privacy Policy";
      }
      break;
  }
};

const submitForm = () => {
  Object.keys(form.value).forEach(validateField);

  if (isFormValid.value) {
    // Here you would typically send the form data to your server
    console.log("Form submitted:", form.value);
    alert(
      "You're registered! You'll receive an email with more details on the event shortly."
    );
    // Reset form after submission
    Object.keys(form.value).forEach((key) => {
      if (typeof form.value[key] === "boolean") {
        form.value[key] = false;
      } else {
        form.value[key] = "";
      }
    });
  } else {
    alert("Please fill out all required fields correctly before submitting.");
  }
};
</script>
