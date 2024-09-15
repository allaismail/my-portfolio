<template>
    <div class="skills-section">
      <h2>Skills</h2>
      <ul class="skills-list">
        <li v-for="(skill, index) in skills" :key="index" class="skill-item">
          {{ skill }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SkillsSection',
    props: {
      skills: Array
    }
  }
  </script>
  
  <style scoped>
  .skills-section {
    margin-bottom: 30px;
  }
  
  h2 {
    color: #0066cc;
    font-size: 24px;
    margin-bottom: 20px;
  }
  
  .skills-list {
    list-style-type: none;
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  
  .skill-item {
    background-color: #e6f2ff;
    color: #0066cc;
    padding: 8px 15px;
    border-radius: 20px;
    font-size: 14px;
  }
  </style>