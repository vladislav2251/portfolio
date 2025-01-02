<template>
    <Container>
      <ProjectCard
        :number="element.number"
        :label="element.label"
        :description="element.description"
        :detail="element.detail"
        :path="element.path"
        :link="element.link"
        :src="element.src"
        v-for="(element, i) in projects"
        :key="i"
      />
    </Container>
  </template>
  
  <script setup lang="ts">
  import Container from '@/components/ui/container.vue';
  import ProjectCard from '@/components/project_card.vue';
  
  import { ref } from 'vue';
  
  const projects = ref([
    { 
      number: "01",
      label: "MARGANETS_STUDIOS", 
      description: "I consistently communicated with clients, addressing project-related issues. I oversaw projects from inception to launch, ensuring smooth execution.", 
      detail: `
        - New web development technologies such as Nuxt.js, Docker, Prisma REST APIs, and more.
        - Developed and maintained user interfaces using Vue.js.
        - Conducted code reviews and participated in architectural discussions.
        - Fixed bugs and resolved issues identified during testing.
        - Mentored and trained junior developers.`,
      path: "https://github.com/vladislav2251/marganets-studios", 
      src: "/img/Block.jpg",
      link: ""
    },
    { 
      number: "02",
      label: "Spotify - Clone", 
      description: "A Spotify clone using Vue.js for the frontend and Prisma ORM for the backend.", 
      detail: `
        - Explored music player functions and learned about new libraries.
      `,
      path: "https://github.com/vladislav2251/spotify-clone", 
      src: "/img/Block2.jpg",
      link: ""
    },
    {
      number: "03",
      label: "E-SHOPR",
      description: "I developed an e-commerce website that provides users with a convenient and intuitive interface for shopping. The project covers the entire cycle from product catalog to order processing.",
      detail: `
        - Modern, custom design.
        - Responsive & accessible.
        - Animations & interactions
        - Engaging user expirience
      `,
      path: "https://github.com/vladislav2251/SHOPR-E-Commerce-Website",
      src: "/img/Block3.jpg",
      link: ""
    }
  ]);
  </script>
  