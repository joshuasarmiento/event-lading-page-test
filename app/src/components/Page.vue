<template>
  <header class="max-w-7xl mx-auto bg-white shadow-sm">
    <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
      <img src="../assets/DarkLogo.webp" alt="TaskUs Logo" class="h-6" />
      <div class="space-x-8 hidden md:block">
        <a href="#" class="text-block text-[14px]">Why TaskUs?</a>
        <a href="#" class="text-block text-[14px]">Services</a>
        <a href="#" class="text-block text-[14px]">Industries</a>
        <a href="#" class="text-block text-[14px]">Location</a>
        <a href="#" class="text-block text-[14px]">Insights</a>
      </div>
      <div class="space-x-4 hidden md:block">
        <button
          class="px-6 py-2.5 text-sm text-[#065BFF] border border-[#065BFF] rounded-full hover:bg-blue-50"
        >
          Contact Us
        </button>
        <button
          class="px-6 py-2.5 text-sm bg-[#065BFF] text-white rounded-full hover:bg-blue-700"
        >
          Try Assist AI
        </button>
      </div>
      <div class="block md:hidden">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 32 32"
        >
          <path
            fill="none"
            stroke="#000000"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M5 8h22M5 16h22M5 24h22"
          />
        </svg>
      </div>
    </nav>
  </header>

  <div class="min-h-screen">
    <!-- Hero Section -->
    <section class="bg-[#065BFF]/20">
      <div
        class="container h-full md:h-screen max-w-7xl mx-auto flex flex-col sm:flex-row items-center"
      >
        <div class="w-full md:w-1/2 p-12 md:pr-8">
          <p class="text-sm text-[#065BFF] font-semibold mb-2">
            Forward TaskUs Webinar Series
          </p>
          <h1 class="text-[48px] font-bold mb-4">How to Integrate GenAI into CX:</h1>
          <h2 class="text-[24px] font-semibold mb-4">
            Balancing Innovation with Safety & Security
          </h2>
          <p class="text-sm mb-4 text-[#495057]">April 30, 2024, 11:00 AM PDT</p>
          <button
            class="px-6 py-3 bg-[#FF0074] text-white rounded-full text-sm font-normal hover:bg-pink-600"
          >
            REGISTER NOW
          </button>
        </div>
        <div class="hidden md:block w-1/2 relative">
          <img src="../assets/image1.png" alt="People discussing" class="" />
        </div>
      </div>
    </section>

    <section class="bg-[#F8F9FA]">
      <div
        class="container max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 md:gap-20 py-20"
      >
        <!-- Webinar Details -->
        <div class="p-12 md:p-0">
          <div class="">
            <p class="text-sm text-[#065BFF] font-semibold mb-2">Webinar</p>
            <h3 class="text-3xl font-semibold mb-2">How to Integrate GenAI into CX:</h3>
            <p class="text-[20px] font-semibold mb-1">
              Balancing Innovation with Safety & Security
            </p>
            <span>April 30, 2024, 11:00 AM PDT</span>
            <div class="flex mt-2 gap-4 mb-4">
              <div class="flex items-center justify-center space-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-[#065BFF]"
                  viewBox="0 0 24 24"
                >
                  <path
                    fill="#065BFF"
                    d="M12 12q.825 0 1.413-.587T14 10t-.587-1.412T12 8t-1.412.588T10 10t.588 1.413T12 12m0 10q-4.025-3.425-6.012-6.362T4 10.2q0-3.75 2.413-5.975T12 2t5.588 2.225T20 10.2q0 2.5-1.987 5.438T12 22"
                  />
                </svg>
                <span>Zoom</span>
              </div>
              <div class="flex items-center justify-center space-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 text-[#065BFF]"
                  viewBox="0 0 24 24"
                >
                  <path
                    fill="#065BFF"
                    d="M13 12.6V9q0-.425-.288-.712T12 8t-.712.288T11 9v3.975q0 .2.075.388t.225.337l2.8 2.8q.275.275.7.275t.7-.275t.275-.7t-.275-.7zM12 22q-1.875 0-3.512-.712t-2.85-1.925t-1.925-2.85T3 13t.713-3.512t1.924-2.85t2.85-1.925T12 4t3.513.713t2.85 1.925t1.925 2.85T21 13t-.712 3.513t-1.925 2.85t-2.85 1.925T12 22M2.05 7.3q-.275-.275-.275-.7t.275-.7L4.9 3.05q.275-.275.7-.275t.7.275t.275.7t-.275.7L3.45 7.3q-.275.275-.7.275t-.7-.275m19.9 0q-.275.275-.7.275t-.7-.275L17.7 4.45q-.275-.275-.275-.7t.275-.7t.7-.275t.7.275l2.85 2.85q.275.275.275.7t-.275.7"
                  />
                </svg>
                <span>40 mins</span>
              </div>
            </div>
            <div class="h-0.5 my-10 bg-black w-full"></div>
            <p class="">
              GenAI can help streamline processes and free people to do more complex work,
              leading to a better customer experience (CX). But security is paramount.
            </p>
            <p class="mb-4">How can companies balance both?</p>
            <p class="mb-4">
              In this webinar, a panel of experts and enterprise leaders will discuss best
              practices and real-world use cases, including:
            </p>
            <ul class="list-disc list-inside mb-4">
              <li>How to implement and optimize GenAI in CX, securely</li>
              <li>
                Why humans and AI working together is the only way to unlock the
                technology's full potential
              </li>
              <li>
                The role of Trust & Safety and Risk & Response in your GenAI strategy
              </li>
            </ul>
          </div>
        </div>

        <!-- Registration Form -->
        <div class="p-12 md:p-0">
          <Registrationfrom />
        </div>
      </div>
    </section>

    <!-- Speakers -->
    <section class="container bg-white max-w-7xl mx-auto py-20">
      <h3 class="text-2xl font-semibold text-center uppercase mb-10">Speakers</h3>
      <div class="grid grid-cols-1 gap-8 mx-4 sm:mx-0">
        <div
          v-for="speaker in speakers"
          :key="speaker.name"
          class="border rounded-2xl p-12"
        >
          <div class="flex flex-col sm:flex-row items-start sm:items-center">
            <div class="mr-12 mb-6 sm:mb-0">
              <img
                :src="speaker.image"
                :alt="speaker.name"
                class="h-40 sm:h-full object-cover mx-auto"
              />
            </div>
            <div>
              <h4 class="text-[20px] font-semibold mb-2">{{ speaker.name }}</h4>
              <p class="text-block mb-2 text-sm">{{ speaker.title }}</p>
              <p class="text-block mb-4 text-sm">{{ speaker.company }}</p>
              <p class="text-normal">{{ speaker.bio }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <footer class="bg-black">
    <div
      class="mx-auto max-w-screen-xl space-y-8 px-4 py-16 sm:px-6 lg:space-y-16 lg:px-8"
    >
      <div class="grid grid-cols-1 gap-8 lg:grid-cols-3">
        <div>
          <div class="">
            <img src="../assets/LightLogo.webp" alt="TaskUs Logo" class="h-8 mb-4" />
          </div>

          <p class="mt-4 max-w-xs text-white">
            We exist to empower people to deliver effortless Digital CX innovation to the
            world's best companies.
          </p>
        </div>

        <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:col-span-2 lg:grid-cols-3">
          <div>
            <p class="font-medium text-white">Contact</p>

            <ul class="mt-6 space-y-4 text-sm">
              <li>
                <a href="#" class="text-white transition hover:opacity-75"> Security </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  Contact Us
                </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75"> Phone </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75"> Support </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  sales@taskus.com
                </a>
              </li>
            </ul>
          </div>

          <div>
            <p class="font-medium text-white">Useful Links</p>

            <ul class="mt-6 space-y-4 text-sm">
              <li>
                <a href="#" class="text-white transition hover:opacity-75"> Out Story </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  Our Advantage
                </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  Leadership
                </a>
              </li>
            </ul>
          </div>

          <div>
            <p class="font-medium text-white">Industries</p>

            <ul class="mt-6 space-y-4 text-sm">
              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  Entertainment + Gaming
                </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75"> FinTech </a>
              </li>

              <li>
                <a href="#" class="text-white transition hover:opacity-75">
                  HealthTech
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>

      <p class="text-xs text-white">&copy; 2023 TaskUs. All rights reserved.</p>
    </div>
  </footer>
</template>

<script setup>
import { ref, computed } from "vue";
import image2 from "../assets/image2.png";
import Registrationfrom from "./RegistrationForm.vue";

const speakers = ref([
  {
    name: "Anita Tomlinson",
    title: "VP, Head of Customer Operations",
    company: "ABC Company",
    image: image2,
    bio:
      "Anita is a customer service and financial services expert who focuses on delivering exceptional experiences. She prioritizes customer needs and drives operational excellence through process optimization and innovative solutions.",
  },
  {
    name: "Archie Jackson",
    title: "SVP, Global Offerings",
    company: "X Company",
    image: image2,
    bio:
      "Archie oversees X' global offerings, including Trust + Safety, AI Services, Digital Customer Experience, and Risk + Response. With 20+ years of experience, he creates digital solutions and advocates for better mental health in the workplace.",
  },
  {
    name: "Amos Pandya",
    title: "DVP, Digital",
    company: "X Company",
    image: image2,
    bio:
      "Amos has 28 years of experience in contact center technology, leading and designing innovative and scalable digital solutions to increase growth, efficiency, and customer satisfaction for businesses and their customers.",
  },
]);
</script>
