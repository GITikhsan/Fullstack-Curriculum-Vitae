<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'
import SectionTitle from './SectionTitle.vue'
// const skills = ref([])
// onMounted(async () => {
//     try {
//         const response = await axios.get('http://localhost:3000/api/skills')
//         skills.value = response.data
//     } catch (error) {
//         console.error(error)
//     }
// })

// const skills = ref([]);
// const API_URL = import.meta.env.PROD ? '/api/skills' :
// 'http://localhost:3000/api/skills';
// onMounted(async () => {
// try {
// skills.value = (await axios.get(API_URL)).data;
// } catch (error) {
// console.error('Gagal mengambil data skill:', error);
// }
// });

const skills = [
  {
    name: 'JavaScript',
    level: 'intermediate',
    image: 'https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png'
  },
  {
    name: 'Vue.js',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/9/95/Vue.js_Logo_2.svg'
  },
  {
    name: 'Laravel',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg'
  },
  {
    name: 'Express.js',
    level: 'intermediate',
    image: 'https://upload.wikimedia.org/wikipedia/commons/6/64/Expressjs.png'
  },
  {
    name: 'Node.js',
    level: 'intermediate',
    image: 'https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg'
  },
  {
    name: 'Tailwind CSS',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg'
  },
  {
    name: 'Bootstrap CSS',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/b/b2/Bootstrap_logo.svg'
  },
  {
    name: 'HTML5',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg'
  },
  {
    name: 'CSS3',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg'
  },
  {
    name: 'C#',
    level: 'intermediate',
    image: 'https://upload.wikimedia.org/wikipedia/commons/4/4f/Csharp_Logo.png'
  },
  {
    name: 'MYSQL',
    level: 'intermediate',
    image: 'https://upload.wikimedia.org/wikipedia/en/d/dd/MySQL_logo.svg'
  },
  {
    name: 'Git & GitHub',
    level: 'proficient',
    image: 'https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg'
  }
];
</script>

<template>
    <section id="skill" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <SectionTitle title="Expertise and Technology" />
            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 md:gap-8"
            >
                <div
                    
                    v-for="skill in skills"
                    :key="skill.name"
                    class="bg-white p-5 sm:p-6 rounded-xl shadow-lg text-center flex flex-col items-center transition-transform duration-300 hover:-translate-y-2 hover:shadow-2xl"
                >
                <img class ="w-16 h-16 sm:w-20 sm:h-20 mb-4" :src="skill.image" :alt="skill.image" />
                    <h3 class="text-lg sm:text-xl font-bold text-gray-800 break-words">
                        {{ skill.name }}
                    </h3>
                    <p class="text-gray-500 mt-2 text-sm sm:text-base">
                        {{ skill.level }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>
