<template>
    <div class="experience-section">
      <h2>Professional Experience</h2>
      <div v-for="(exp, index) in experiences" :key="index" class="experience-item">
        <h3>{{ exp.title }}</h3>
        <p class="company-period">{{ exp.company }} | {{ exp.period }}</p>
        <ul>
          <li v-for="(resp, respIndex) in exp.responsibilities" :key="respIndex">
            {{ resp }}
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ExperienceSection',
    props: {
      experiences: Array
    }
  }
  </script>
  
  <style scoped>
  .experience-section {
    margin-bottom: 30px;
  }
  
  .experience-item {
    margin-bottom: 20px;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
  }
  
  h2 {
    color: #0066cc;
    font-size: 24px;
    margin-bottom: 20px;
  }
  
  h3 {
    color: #333;
    font-size: 20px;
    margin-bottom: 10px;
  }
  
  .company-period {
    font-style: italic;
    color: #666;
    margin-bottom: 10px;
  }
  
  ul {
    padding-left: 20px;
  }
  
  li {
    margin-bottom: 5px;
  }
  </style>