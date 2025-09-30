<template>
  <section id="skills" class="skills">
    <div class="container">
      <h2 class="section-title">Skills</h2>
      <div class="skills-grid">
        <div class="skill-category">
          <h3 class="category-title">Frontend</h3>
          <div class="skill-items">
            <div
              class="skill-item"
              v-for="skill in frontendSkills"
              :key="skill.name"
            >
              <div class="skill-info">
                <span class="skill-name">{{ skill.name }}</span>
                <span class="skill-percentage">{{ skill.level }}%</span>
              </div>
              <div class="skill-bar">
                <div
                  class="skill-progress"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <div class="skill-category">
          <h3 class="category-title">Backend</h3>
          <div class="skill-items">
            <div
              class="skill-item"
              v-for="skill in backendSkills"
              :key="skill.name"
            >
              <div class="skill-info">
                <span class="skill-name">{{ skill.name }}</span>
                <span class="skill-percentage">{{ skill.level }}%</span>
              </div>
              <div class="skill-bar">
                <div
                  class="skill-progress"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <div class="skill-category">
          <h3 class="category-title">Tools & Others</h3>
          <div class="skill-items">
            <div
              class="skill-item"
              v-for="skill in toolSkills"
              :key="skill.name"
            >
              <div class="skill-info">
                <span class="skill-name">{{ skill.name }}</span>
                <span class="skill-percentage">{{ skill.level }}%</span>
              </div>
              <div class="skill-bar">
                <div
                  class="skill-progress"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const frontendSkills = ref([
  { name: "Vue.js", level: 90 },
  { name: "React", level: 85 },
  { name: "TypeScript", level: 80 },
  { name: "JavaScript", level: 95 },
  { name: "CSS/SCSS", level: 88 },
  { name: "HTML5", level: 92 },
]);

const backendSkills = ref([
  { name: "Node.js", level: 85 },
  { name: "Express", level: 80 },
  { name: "Python", level: 75 },
  { name: "MongoDB", level: 78 },
  { name: "PostgreSQL", level: 70 },
  { name: "REST API", level: 88 },
]);

const toolSkills = ref([
  { name: "Git", level: 90 },
  { name: "Docker", level: 65 },
  { name: "AWS", level: 60 },
  { name: "Figma", level: 75 },
  { name: "VS Code", level: 95 },
  { name: "Linux", level: 70 },
]);
</script>

<style scoped>
.skills {
  padding: 5rem 0;
  background-color: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 3rem;
  color: #333;
  position: relative;
}

.section-title::after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 4px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 2px;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 3rem;
}

.skill-category {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.category-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  color: #333;
  text-align: center;
}

.skill-items {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-item {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.skill-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.skill-name {
  font-weight: 500;
  color: #333;
}

.skill-percentage {
  font-weight: 600;
  color: #667eea;
}

.skill-bar {
  height: 8px;
  background-color: #e0e0e0;
  border-radius: 4px;
  overflow: hidden;
}

.skill-progress {
  height: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 4px;
  transition: width 1s ease-in-out;
}

@media (max-width: 768px) {
  .skills-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .skill-category {
    padding: 1.5rem;
  }
}
</style>
