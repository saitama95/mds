<template>
  <div class="bg-gradient-to-br from-gray-50 to-white">
    <!-- Hero Section -->
    <section id="home" class="py-20 md:py-28">
      <div class="container mx-auto px-4 md:px-6 max-w-7xl">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Left Content -->
          <div>
            <div class="inline-block bg-blue-50 text-blue-700 px-4 py-2 rounded-full text-sm font-semibold mb-6">
              ✦ Digital Growth Partner
            </div>
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight mb-6">
              Our Collaboration Makes a 
              <span class="text-blue-600 border-b-4 border-blue-600 inline-block">Success Path</span> 
              For Your Brand!
            </h1>
            <p class="text-xl text-gray-600 mb-8">
              Make Your Brand <strong class="font-bold text-gray-900">Impossible to Ignore!</strong> Grow with 
              <span class="font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
                Mishra Digital Solution
              </span>
            </p>
            <div class="flex flex-wrap gap-4 mb-8">
              <button 
                @click="scrollToSection('contact')" 
                class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-full font-semibold shadow-lg hover:shadow-xl transform hover:-translate-y-0.5 transition-all duration-200"
              >
                Start Growing →
              </button>
              <button 
                @click="scrollToSection('services')" 
                class="border-2 border-gray-300 hover:border-blue-600 text-gray-700 hover:text-blue-600 px-8 py-3 rounded-full font-semibold transition-all duration-200"
              >
                Explore Services
              </button>
            </div>
            <div class="inline-flex items-center gap-3 bg-gray-100 px-5 py-2 rounded-full">
              <span class="text-xl">📱</span>
              <span class="font-medium text-gray-700">{{ contactInfo.insta }}</span>
            </div>
          </div>

          <!-- Right Visual -->
          <div>
            <div class="bg-white rounded-3xl p-8 shadow-2xl border border-gray-100">
              <div class="grid grid-cols-2 gap-6 mb-6">
                <div v-for="stat in stats" :key="stat.label" class="text-center">
                  <div class="text-3xl md:text-4xl font-extrabold text-blue-600">{{ stat.value }}</div>
                  <div class="text-sm text-gray-500 mt-1">{{ stat.label }}</div>
                </div>
              </div>
              <div class="text-center font-semibold text-gray-800 pt-4 border-t border-gray-100">
                #DigitalExcellence
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-20 bg-white">
      <div class="container mx-auto px-4 md:px-6 max-w-7xl">
        <div class="text-center max-w-2xl mx-auto mb-16">
          <span class="inline-block bg-blue-50 text-blue-600 px-4 py-2 rounded-full text-sm font-semibold mb-4">
            What We Deliver
          </span>
          <h2 class="text-3xl md:text-4xl font-extrabold mb-4">Comprehensive Creative & Digital Solutions</h2>
          <p class="text-gray-600 text-lg">From logo design to 3D AutoCAD, we craft brand experiences that captivate.</p>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
          <div 
            v-for="(service, idx) in servicesList" 
            :key="idx" 
            class="bg-gray-50 hover:bg-blue-50 p-5 rounded-2xl text-center transition-all duration-300 cursor-pointer hover:shadow-lg hover:-translate-y-1"
          >
            <div class="text-3xl mb-3">✨</div>
            <h3 class="font-semibold text-gray-800 text-sm md:text-base">{{ service }}</h3>
          </div>
        </div>

        <div class="text-center mt-10">
          <p class="text-gray-500 font-medium">➕ And more: Social Media Promotion, Digital Marketing, Packaging & Branding</p>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gradient-to-br from-gray-50 to-blue-50/30">
      <div class="container mx-auto px-4 md:px-6 max-w-7xl">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Left Illustration -->
          <div>
            <div class="bg-gradient-to-br from-blue-100 to-indigo-100 rounded-3xl p-12 text-center shadow-xl">
              <div class="inline-block bg-white/80 backdrop-blur px-6 py-2 rounded-full font-bold text-gray-800 mb-8">
                🚀 innovation
              </div>
              <div class="text-3xl md:text-4xl font-extrabold text-gray-800">
                Collaboration → Success
              </div>
            </div>
          </div>

          <!-- Right Content -->
          <div>
            <span class="inline-block bg-blue-50 text-blue-600 px-4 py-2 rounded-full text-sm font-semibold mb-4">
              Why Partner With Us
            </span>
            <h2 class="text-3xl md:text-4xl font-extrabold mb-4">Your Success is Our Blueprint</h2>
            <p class="text-gray-600 text-lg mb-6">
              At Mishra Digital Solution, we blend creative design, strategic digital marketing, and cutting-edge technology to make brands unstoppable. Every project is a partnership — we listen, ideate, and execute with precision.
            </p>
            <div class="flex flex-wrap gap-3 mb-8">
              <div class="bg-white px-4 py-2 rounded-full shadow-sm">✅ 360° Branding & Design</div>
              <div class="bg-white px-4 py-2 rounded-full shadow-sm">✅ Result-Driven Digital Marketing</div>
              <div class="bg-white px-4 py-2 rounded-full shadow-sm">✅ UI/UX & Development Ready</div>
              <div class="bg-white px-4 py-2 rounded-full shadow-sm">✅ Dedicated Support & Fast Turnaround</div>
            </div>
            <div class="border-l-4 border-blue-600 pl-6 py-2">
              <p class="text-xl font-bold italic text-gray-800">"Our Collaboration Makes a Success Path For Your Brand"</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-white">
      <div class="container mx-auto px-4 md:px-6 max-w-7xl">
        <div class="grid md:grid-cols-2 gap-12">
          <!-- Left Contact Info -->
          <div>
            <span class="inline-block bg-blue-50 text-blue-600 px-4 py-2 rounded-full text-sm font-semibold mb-4">
              Let's Connect
            </span>
            <h2 class="text-3xl md:text-4xl font-extrabold mb-4">Ready to make your brand impossible to ignore?</h2>
            <p class="text-gray-600 text-lg mb-8">Reach out and let's craft your success story.</p>
            
            <div class="space-y-6">
              <div class="flex items-start gap-4">
                <span class="text-3xl">📞</span>
                <div>
                  <strong class="block text-gray-900">Call / WhatsApp</strong>
                  <p class="text-gray-600">{{ contactInfo.phone1 }}</p>
                  <p class="text-gray-600">{{ contactInfo.phone2 }}</p>
                </div>
              </div>
              <div class="flex items-center gap-4">
                <span class="text-3xl">✉️</span>
                <div>
                  <strong class="block text-gray-900">Email</strong>
                  <p class="text-gray-600">{{ contactInfo.email }}</p>
                </div>
              </div>
              <div class="flex items-center gap-4">
                <span class="text-3xl">🌐</span>
                <div>
                  <strong class="block text-gray-900">Instagram</strong>
                  <p class="text-gray-600">{{ contactInfo.insta }}</p>
                </div>
              </div>
            </div>

            <div class="flex gap-4 mt-8">
              <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Instagram →</a>
              <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">LinkedIn →</a>
              <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Behance →</a>
            </div>
          </div>

          <!-- Right Contact Form -->
          <div class="bg-gray-50 rounded-3xl p-8 shadow-lg border border-gray-100">
            <h3 class="text-2xl font-bold mb-6">Send a Message</h3>
            <form @submit.prevent="handleSubmit" class="space-y-4">
              <input 
                v-model="formData.name"
                type="text" 
                placeholder="Your Name" 
                required
                class="w-full px-5 py-3 rounded-full border border-gray-200 focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200 transition"
              >
              <input 
                v-model="formData.email"
                type="email" 
                placeholder="Email Address" 
                required
                class="w-full px-5 py-3 rounded-full border border-gray-200 focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200 transition"
              >
              <input 
                v-model="formData.phone"
                type="tel" 
                placeholder="Phone Number"
                class="w-full px-5 py-3 rounded-full border border-gray-200 focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200 transition"
              >
              <textarea 
                v-model="formData.message"
                rows="4" 
                placeholder="Tell us about your project..."
                class="w-full px-5 py-3 rounded-2xl border border-gray-200 focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-200 transition resize-none"
              ></textarea>
              <button 
                type="submit" 
                class="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 rounded-full font-semibold shadow-md hover:shadow-lg transition-all duration-200"
              >
                Get in Touch →
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// TypeScript Interfaces
interface ContactInfo {
  phone1: string
  phone2: string
  email: string
  insta: string
}

interface FormData {
  name: string
  email: string
  phone: string
  message: string
}

// Data
const servicesList = ref<string[]>([
  "Logo Design", "Banner Design", "Social Media Post & Promotion", "Website & App UI Design",
  "Flyer Design", "Brochure Design", "Icon & Catalogue Design", "Digital Marketing & Promotion",
  "AutoCAD 2D & 3D Designing", "Video Editing", "Festival Post Design", "Branding & Packaging Design",
  "Letter Head & Invitation Card Design"
])

const stats = ref([
  { value: "500+", label: "Projects Delivered" },
  { value: "120+", label: "Happy Brands" },
  { value: "24/7", label: "Support" },
  { value: "4.9", label: "Client Rating" }
])

const contactInfo = ref<ContactInfo>({
  phone1: "+91 3453457805",
  phone2: "+91 912545697",
  email: "mishraDigitalPoint@gmail.com",
  insta: "@mishradigitalsolution"
})

const formData = ref<FormData>({
  name: '',
  email: '',
  phone: '',
  message: ''
})

// Methods
const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth', block: 'start' })
  }
}

const handleSubmit = () => {
  alert(`Thanks ${formData.value.name}! We'll contact you soon at ${formData.value.email}`)
  formData.value = { name: '', email: '', phone: '', message: '' }
}
</script>

<style scoped>
/* Any additional custom styles beyond Tailwind can go here */
/* Tailwind already handles most styling, so this can be minimal */

/* Smooth scroll behavior for the whole page */
html {
  scroll-behavior: smooth;
}
</style>