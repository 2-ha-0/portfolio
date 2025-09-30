<template>
  <section id="skills" class="skills">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Skills</h2>
        <p class="section-subtitle">보유 기술과 숙련도</p>
      </div>

      <div class="skills-container">
        <div class="skill-category">
          <div class="category-header">
            <div class="category-icon">🎨</div>
            <h3 class="category-title">Frontend</h3>
          </div>
          <div class="skill-list">
            <div class="skill-item">
              <span class="skill-name">Vue.js</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 95%"></div>
              </div>
              <span class="skill-percentage">95%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">React</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 90%"></div>
              </div>
              <span class="skill-percentage">90%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">TypeScript</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 85%"></div>
              </div>
              <span class="skill-percentage">85%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">JavaScript</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 98%"></div>
              </div>
              <span class="skill-percentage">98%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">CSS/SCSS</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 92%"></div>
              </div>
              <span class="skill-percentage">92%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">HTML5</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 95%"></div>
              </div>
              <span class="skill-percentage">95%</span>
            </div>
          </div>
        </div>

        <div class="skill-category">
          <div class="category-header">
            <div class="category-icon">⚙️</div>
            <h3 class="category-title">Backend</h3>
          </div>
          <div class="skill-list">
            <div class="skill-item">
              <span class="skill-name">Node.js</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 90%"></div>
              </div>
              <span class="skill-percentage">90%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">Express</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 88%"></div>
              </div>
              <span class="skill-percentage">88%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">Python</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 80%"></div>
              </div>
              <span class="skill-percentage">80%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">MongoDB</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 85%"></div>
              </div>
              <span class="skill-percentage">85%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">PostgreSQL</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 75%"></div>
              </div>
              <span class="skill-percentage">75%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">REST API</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 92%"></div>
              </div>
              <span class="skill-percentage">92%</span>
            </div>
          </div>
        </div>

        <div class="skill-category">
          <div class="category-header">
            <div class="category-icon">🛠️</div>
            <h3 class="category-title">Tools & Others</h3>
          </div>
          <div class="skill-list">
            <div class="skill-item">
              <span class="skill-name">Git</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 95%"></div>
              </div>
              <span class="skill-percentage">95%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">Docker</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 70%"></div>
              </div>
              <span class="skill-percentage">70%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">AWS</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 65%"></div>
              </div>
              <span class="skill-percentage">65%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">Figma</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 80%"></div>
              </div>
              <span class="skill-percentage">80%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">VS Code</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 98%"></div>
              </div>
              <span class="skill-percentage">98%</span>
            </div>
            <div class="skill-item">
              <span class="skill-name">Linux</span>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 75%"></div>
              </div>
              <span class="skill-percentage">75%</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const skillCategories = ref([
  {
    name: "Frontend",
    icon: "🎨",
    skills: [
      { name: "Vue.js", level: 95 },
      { name: "React", level: 90 },
      { name: "TypeScript", level: 85 },
      { name: "JavaScript", level: 98 },
      { name: "CSS/SCSS", level: 92 },
      { name: "HTML5", level: 95 },
    ],
  },
  {
    name: "Backend",
    icon: "⚙️",
    skills: [
      { name: "Node.js", level: 90 },
      { name: "Express", level: 88 },
      { name: "Python", level: 80 },
      { name: "MongoDB", level: 85 },
      { name: "PostgreSQL", level: 75 },
      { name: "REST API", level: 92 },
    ],
  },
  {
    name: "Tools & Others",
    icon: "🛠️",
    skills: [
      { name: "Git", level: 95 },
      { name: "Docker", level: 70 },
      { name: "AWS", level: 65 },
      { name: "Figma", level: 80 },
      { name: "VS Code", level: 98 },
      { name: "Linux", level: 75 },
    ],
  },
]);
</script>

<style scoped>
.skills {
  padding: 6rem 0;
  background: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
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

.section-subtitle {
  font-size: 1.1rem;
  color: #666;
  font-weight: 500;
}

.skills-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.skill-category {
  background: #f8f9fa;
  border-radius: 15px;
  padding: 1.5rem;
  transition: all 0.3s ease;
}

.skill-category:hover {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.category-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.category-icon {
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
  color: white;
  box-shadow: 0 4px 10px rgba(102, 126, 234, 0.3);
}

.category-title {
  font-size: 1.2rem;
  font-weight: 600;
  color: #1f2937;
  margin: 0;
}

.skill-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.skill-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0.8rem;
  background: white;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}

.skill-item:hover {
  transform: translateX(5px);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.skill-name {
  font-size: 0.9rem;
  font-weight: 600;
  color: #374151;
  min-width: 80px;
}

.skill-bar {
  flex: 1;
  height: 8px;
  background: #e5e7eb;
  border-radius: 10px;
  overflow: hidden;
  position: relative;
}

.skill-progress {
  height: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 10px;
  transition: width 1.5s ease-in-out;
  position: relative;
}

.skill-progress::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent 0%,
    rgba(255, 255, 255, 0.3) 50%,
    transparent 100%
  );
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

.skill-percentage {
  font-size: 0.8rem;
  font-weight: 600;
  color: #667eea;
  min-width: 35px;
  text-align: right;
}

@media (max-width: 768px) {
  .skills-container {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .container {
    padding: 0 1rem;
  }

  .section-title {
    font-size: 2rem;
  }
}
</style>
