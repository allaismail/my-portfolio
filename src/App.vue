<template>
  <div id="app">
    <header>
      <h1>{{ yourName }}'s Portfolio</h1>
      <p>{{ jobTitle }}</p>
    </header>
    <nav>
      <button @click="currentSection = 'experience'" :class="{ active: currentSection === 'experience' }">Experience</button>
      <button @click="currentSection = 'projects'" :class="{ active: currentSection === 'projects' }">Projects</button>
      <button @click="currentSection = 'skills'" :class="{ active: currentSection === 'skills' }">Skills</button>
    </nav>
    <main>
      <ExperienceSection v-if="currentSection === 'experience'" :experiences="experiences" />
      <ProjectsSection v-if="currentSection === 'projects'" :projects="projects" />
      <SkillsSection v-if="currentSection === 'skills'" :skills="skills" />
    </main>
  </div>
</template>

<script>
import ExperienceSection from './components/ExperienceSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue'

export default {
  name: 'App',
  components: {
    ExperienceSection,
    ProjectsSection,
    SkillsSection
  },
  data() {
    return {
      yourName: 'ALLA Ismail',
      jobTitle: 'Cloud Development Engineer',
      currentSection: 'experience',
      experiences: [
        {
          title: "Cloud Development Engineer",
          company: "AT SECURE-IC Oujda",
          period: "04-09-2023 - Present",
          responsibilities: [
            "Drafted specifications and designs for microservices tailored for cloud environments.",
            "Developed and tested microservices using FastAPI, PostgreSQL and VueJS.",
            "Deployed microservices using Docker, Kubernetes, Helm and Ansible.",
            "Managed source code versioning with Git and GitLab, and created CI/CD pipelines using GitLab CI for automated testing and deployment.",
            "Implemented secure RESTful APIs through authentication and authorization best practices with IAM tools by using Keycloak and JWT.",
            "Collaborated on integrating microservices to ensure cohesive functionality."
          ]
        },
        {
          title: "Cloud Development Engineer Intern",
          company: "AT SECURE-IC Oujda",
          period: "13-02-2023 - 30-07-2023",
          responsibilities: [
            "Studied LoadBalancers for LwM2M protocol for both on-premise and cloud providers.",
            "Designed and implemented a scalable architecture for IoT systems within a K8S cluster.",
            "Developed an LwM2M emulation client to perform load tests on the LwM2M server by modifying the Leshan client source code.",
            "Deployed the solution in Kubernetes both on-premise and in cloud providers (Aws and Azure) using their LoadBalancers for UDP.",
            "Technologies used: Kubernetes, Docker, Aws, Azure, Redis, Ingress, Coap, Python, Wsl, SessionAffinity, Java"
          ]
        },
        {
          title: "Cloud Development Engineer Intern",
          company: "AT SECURE-IC Oujda",
          period: "04-07-2022 - 31-08-2022",
          responsibilities: [
            "Contributed to the project specification design, employing FastAPI for backend development.",
            "Used PostgreSQL for database management, and Vue.js for frontend development.",
            "Developed the application and orchestrated microservices within Kubernetes clusters.",
            "Managed the containerization and deployment processes using Docker to ensure consistent environments.",
            "Integrated Keycloak for security."
          ]
        }
      ],
      projects: [
        {
          title: "Creation of a Practical-Work Platform Based in Cloud Computing, ENSAO",
          period: "01-04-2022 - 15-06-2022",
          description: "Developed a SaaS application using OpenStack in a private cloud environment. The application provided students with a service environment to perform their practical work, utilizing Ubuntu, Java/JEE, CSS, HTML, Bootstrap, and MySQL. Integration of Xpra protocol ensured seamless connectivity and service delivery."
        },
        {
          title: "Automatic Authentication Using Computer Vision, ENSAO",
          period: "01-04-2021 - 15-06-2021",
          description: "Developed an automated ID card scanning tool using Python, NumPy, OpenCV, Tkinter, and PyTesseract to extract all necessary information and store it directly in a MySQL database, eliminating the need for manual data entry."
        }
      ],
      skills: [
        "Cloud Platforms: AWS, Azure, OpenStack, Cloud Native",
        "Virtualization: VirtualBox, Hyper-V, Vagrant, Docker",
        "CI/CD: Git, GitHub/Actions, GitLab",
        "Monitoring: Prometheus, Grafana",
        "Orchestration Automation: Kubernetes, Terraform, Ansible, Helm",
        "API and Security: API Design, RESTful Services, API Security, Keycloak, JWT",
        "Networking and Systems: Computer Network, Distributed Systems, Load Balancers, LwM2M, Coap, Wireshark, Harbor Registry",
        "Programming Languages: Python (Django, FastAPI, NumPy, Pandas, Bash scripting), Java/JEE, C, R, JavaScript (Vue.js)",
        "Database Management: MySQL, PostgreSQL, Redis, SQL Server",
        "Development Tools: Visual Studio Code, PyCharm, Eclipse, Windows, Linux, Wsl",
        "Modeling: UML, Merise, Multidimensional Modeling",
        "Data and Machine Learning: Machine Learning, Data Engineering, ETL, Talend, Data Cleaning, MapReduce",
        "Others: knative, YAML, JSON, SSE Event, Cloud Event, Microservices, Bash Scripting"
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

header {
  text-align: center;
  margin-bottom: 30px;
}

h1 {
  color: #0066cc;
  margin-bottom: 10px;
}

nav {
  display: flex;
  justify-content: center;
  margin-bottom: 30px;
}

button {
  background-color: #f0f0f0;
  border: none;
  padding: 10px 20px;
  margin: 0 10px;
  cursor: pointer;
  font-size: 16px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #e0e0e0;
}

button.active {
  background-color: #0066cc;
  color: white;
}

main {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
</style>