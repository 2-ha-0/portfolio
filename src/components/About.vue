<template>
  <section id="about" class="about">
    <div class="container">
      <h2 class="section-title">About Me</h2>
      <div class="about-content">
        <div class="about-text">
          <p>
            안녕하세요! 저는 <strong>5년 경력의 풀스택 개발자</strong>입니다.
            사용자 중심의 웹 애플리케이션 개발에 열정을 가지고 있으며, 최신 기술
            트렌드를 학습하고 적용하는 것을 즐깁니다.
          </p>
          <p>
            <strong>주요 전문 분야:</strong>
          </p>
          <ul class="expertise-list">
            <li>프론트엔드: Vue.js, React, TypeScript</li>
            <li>백엔드: Node.js, Express, Python</li>
            <li>데이터베이스: MongoDB, PostgreSQL</li>
            <li>클라우드: AWS, Vercel, Netlify</li>
          </ul>
          <p>
            팀워크를 중시하며, 코드 품질과 사용자 경험을 최우선으로 생각합니다.
            지속적인 학습과 성장을 통해 더 나은 개발자가 되어가고 있습니다.
          </p>
        </div>
        <div class="about-stats">
          <div class="stat-item">
            <div class="stat-number">5+</div>
            <div class="stat-label">년 경력</div>
          </div>
          <div class="stat-item">
            <div class="stat-number">50+</div>
            <div class="stat-label">프로젝트</div>
          </div>
          <div class="stat-item">
            <div class="stat-number">100%</div>
            <div class="stat-label">만족도</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
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

.about-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 4rem;
  align-items: start;
}

.about-text {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
}

.about-text p {
  margin-bottom: 1.5rem;
}

.expertise-list {
  margin: 1.5rem 0;
  padding-left: 0;
  list-style: none;
}

.expertise-list li {
  padding: 0.5rem 0;
  padding-left: 1.5rem;
  position: relative;
  color: #666;
}

.expertise-list li::before {
  content: "✓";
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
}

.about-stats {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.stat-item {
  text-align: center;
  padding: 2rem;
  background: white;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.stat-item:hover {
  transform: translateY(-5px);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #667eea;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1rem;
  color: #666;
  font-weight: 500;
}

@media (max-width: 768px) {
  .about-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .about-stats {
    flex-direction: row;
    justify-content: space-around;
  }

  .stat-item {
    padding: 1rem;
    flex: 1;
  }

  .stat-number {
    font-size: 2rem;
  }
}
</style>
