<template>
    <div class="projects-section">
      <h2>Projects</h2>
      <div v-for="(project, index) in projects" :key="index" class="project-item">
        <h3>{{ project.title }}</h3>
        <p class="project-period">{{ project.period }}</p>
        <p class="project-description">{{ project.description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProjectsSection',
    props: {
      projects: Array
    }
  }
  </script>
  
  <style scoped>
  .projects-section {
    margin-bottom: 30px;
  }
  
  .project-item {
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
  
  .project-period {
    font-style: italic;
    color: #666;
    margin-bottom: 10px;
  }
  
  .project-description {
    line-height: 1.6;
  }
  </style>