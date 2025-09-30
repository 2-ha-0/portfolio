<template>
  <section id="projects" class="projects">
    <div class="container">
      <h2 class="section-title">Projects</h2>
      <div class="projects-grid">
        <div class="project-card" v-for="project in projects" :key="project.id">
          <div class="project-image">
            <div class="project-placeholder">
              <div class="project-icon">{{ project.icon }}</div>
            </div>
            <div class="project-overlay">
              <a :href="project.demo" target="_blank" class="project-link">
                <span>Demo 보기</span>
              </a>
              <a :href="project.github" target="_blank" class="project-link">
                <span>GitHub</span>
              </a>
            </div>
          </div>
          <div class="project-content">
            <h3 class="project-title">{{ project.title }}</h3>
            <p class="project-description">{{ project.description }}</p>
            <div class="project-tech">
              <span 
                class="tech-tag" 
                v-for="tech in project.technologies" 
                :key="tech"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'E-Commerce Platform',
    description: 'Vue.js와 Node.js를 활용한 풀스택 전자상거래 플랫폼. 결제 시스템, 재고 관리, 사용자 인증 등 완전한 기능을 제공합니다.',
    technologies: ['Vue.js', 'Node.js', 'MongoDB', 'Stripe'],
    icon: '🛒',
    demo: '#',
    github: '#'
  },
  {
    id: 2,
    title: 'Task Management App',
    description: 'React와 TypeScript로 개발한 프로젝트 관리 애플리케이션. 실시간 협업 기능과 드래그 앤 드롭 인터페이스를 제공합니다.',
    technologies: ['React', 'TypeScript', 'Socket.io', 'PostgreSQL'],
    icon: '📋',
    demo: '#',
    github: '#'
  },
  {
    id: 3,
    title: 'Weather Dashboard',
    description: '실시간 날씨 정보와 예보를 제공하는 대시보드. 다양한 차트와 지도 시각화를 포함합니다.',
    technologies: ['Vue.js', 'Chart.js', 'OpenWeather API', 'CSS3'],
    icon: '🌤️',
    demo: '#',
    github: '#'
  },
  {
    id: 4,
    title: 'Social Media Analytics',
    description: '소셜 미디어 데이터 분석 및 시각화 도구. 인스타그램, 트위터 API를 활용한 통계 대시보드입니다.',
    technologies: ['Python', 'Django', 'D3.js', 'Redis'],
    icon: '📊',
    demo: '#',
    github: '#'
  }
])
</script>

<style scoped>
.projects {
  padding: 5rem 0;
  background-color: #f8f9fa;
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
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 4px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 2px;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.project-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.project-image {
  position: relative;
  height: 200px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.project-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
}

.project-icon {
  font-size: 4rem;
  opacity: 0.8;
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-link {
  padding: 0.5rem 1rem;
  background: #667eea;
  color: white;
  text-decoration: none;
  border-radius: 25px;
  font-weight: 500;
  transition: background 0.3s ease;
}

.project-link:hover {
  background: #764ba2;
}

.project-content {
  padding: 1.5rem;
}

.project-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #333;
}

.project-description {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech-tag {
  padding: 0.25rem 0.75rem;
  background: #e9ecef;
  color: #495057;
  border-radius: 15px;
  font-size: 0.875rem;
  font-weight: 500;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
  
  .project-overlay {
    opacity: 1;
    background: rgba(0, 0, 0, 0.6);
  }
}
</style>
