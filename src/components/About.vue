<template>
  <section id="about" class="about">
    <div class="container">
      <div class="about-wrapper">
        <div class="about-left">
          <div class="profile-section">
            <div class="profile-image">
              <div class="image-container">
                <div class="profile-avatar">🧑‍💻</div>
                <div class="status-indicator"></div>
              </div>
            </div>
            <div class="profile-info">
              <h2 class="profile-name">이하영</h2>
              <p class="profile-title">풀스택 개발자</p>
              <!-- <div class="profile-location">
                <span class="location-icon">📍</span>
                <span>서울, 대한민국</span>
              </div> -->
            </div>
          </div>

          <div class="philosophy-section">
            <h3>개발 철학</h3>
            <div class="philosophy-grid">
              <div class="philosophy-item">
                <div class="philosophy-icon">🎯</div>
                <div class="philosophy-content">
                  <h4>사용자 중심</h4>
                  <p>사용자 경험을 최우선으로 생각합니다</p>
                </div>
              </div>
              <div class="philosophy-item">
                <div class="philosophy-icon">🔧</div>
                <div class="philosophy-content">
                  <h4>코드 품질</h4>
                  <p>깔끔하고 유지보수가 쉬운 코드 작성</p>
                </div>
              </div>
              <div class="philosophy-item">
                <div class="philosophy-icon">🚀</div>
                <div class="philosophy-content">
                  <h4>지속적 성장</h4>
                  <p>새로운 기술 학습과 적용을 즐깁니다</p>
                </div>
              </div>
              <div class="philosophy-item">
                <div class="philosophy-icon">🤝</div>
                <div class="philosophy-content">
                  <h4>팀워크</h4>
                  <p>협업을 통한 더 나은 솔루션 구축</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="about-right">
          <div class="bio-section">
            <h3>소개</h3>
            <p>
              5년간의 개발 경험을 바탕으로 사용자 중심의 웹 애플리케이션을
              개발하는 풀스택 개발자입니다. 기술적 완성도와 사용자 경험의 균형을
              맞추며, 지속 가능하고 확장 가능한 코드를 작성하는 것을 목표로
              합니다.
            </p>
            <p>
              새로운 기술을 배우고 적용하는 것을 즐기며, 팀워크를 통해 더 나은
              솔루션을 만들어갑니다. 코드 품질과 사용자 경험을 최우선으로
              생각합니다.
            </p>
          </div>
          <div class="skills-section">
            <h3>기술 스택</h3>
            <div class="skills-container">
              <div class="skill-category">
                <div class="category-header">
                  <div class="category-icon">🎨</div>
                  <h4>Frontend</h4>
                </div>
                <div class="skill-tags">
                  <span class="skill-tag">Vue.js</span>
                  <span class="skill-tag">React</span>
                  <span class="skill-tag">TypeScript</span>
                  <span class="skill-tag">JavaScript</span>
                </div>
              </div>

              <div class="skill-category">
                <div class="category-header">
                  <div class="category-icon">⚙️</div>
                  <h4>Backend</h4>
                </div>
                <div class="skill-tags">
                  <span class="skill-tag">Node.js</span>
                  <span class="skill-tag">Express</span>
                  <span class="skill-tag">Python</span>
                  <span class="skill-tag">REST API</span>
                </div>
              </div>

              <div class="skill-category">
                <div class="category-header">
                  <div class="category-icon">🗄️</div>
                  <h4>Database</h4>
                </div>
                <div class="skill-tags">
                  <span class="skill-tag">MongoDB</span>
                  <span class="skill-tag">PostgreSQL</span>
                  <span class="skill-tag">Redis</span>
                </div>
              </div>

              <div class="skill-category">
                <div class="category-header">
                  <div class="category-icon">🛠️</div>
                  <h4>Tools</h4>
                </div>
                <div class="skill-tags">
                  <span class="skill-tag">Git</span>
                  <span class="skill-tag">Docker</span>
                  <span class="skill-tag">AWS</span>
                  <span class="skill-tag">VS Code</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 6rem 0;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  min-height: 100vh;
  display: flex;
  align-items: center;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.about-wrapper {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 4rem;
  align-items: start;
}

.about-left {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.profile-section {
  background: white;
  border-radius: 20px;
  padding: 2.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  text-align: center;
  position: relative;
  overflow: hidden;
}

.profile-section::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.profile-image {
  margin-bottom: 1.5rem;
}

.image-container {
  position: relative;
  display: inline-block;
}

.profile-avatar {
  width: 120px;
  height: 120px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 3rem;
  color: white;
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
  margin: 0 auto;
}

.status-indicator {
  position: absolute;
  bottom: 10px;
  right: 10px;
  width: 20px;
  height: 20px;
  background: #4ade80;
  border: 3px solid white;
  border-radius: 50%;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.profile-name {
  font-size: 2rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 0.5rem;
}

.profile-title {
  font-size: 1.1rem;
  color: #667eea;
  font-weight: 600;
  margin-bottom: 1rem;
}

.profile-location {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  color: #6b7280;
  font-size: 0.9rem;
}

.location-icon {
  font-size: 1rem;
}

.bio-section {
  background: white;
  border-radius: 20px;
  padding: 2.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.bio-section h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 1.5rem;
  position: relative;
}

.bio-section p {
  font-size: 1rem;
  line-height: 1.7;
  color: #4b5563;
  margin-bottom: 1.5rem;
}

.bio-section p:last-child {
  margin-bottom: 0;
}

.about-right {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.skills-section {
  background: white;
  border-radius: 20px;
  padding: 2.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.skills-section h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 1.5rem;
  position: relative;
}

.skills-container {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-category {
  background: #f8f9fa;
  border-radius: 12px;
  padding: 1.2rem;
  transition: all 0.3s ease;
}

.skill-category:hover {
  background: #e9ecef;
  transform: translateY(-2px);
}

.category-header {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  margin-bottom: 1rem;
}

.category-icon {
  width: 30px;
  height: 30px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1rem;
  color: white;
}

.category-header h4 {
  font-size: 1rem;
  font-weight: 600;
  color: #1f2937;
  margin: 0;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.skill-tag {
  background: #e9ecef;
  color: #495057;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.skill-tag:hover {
  background: #667eea;
  color: white;
  transform: translateY(-1px);
}

.philosophy-section {
  background: white;
  border-radius: 20px;
  padding: 2.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.philosophy-section h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 1.5rem;
  position: relative;
}

.philosophy-grid {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 1.5rem;
}

.philosophy-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.5rem;
  background: #f8f9fa;
  border-radius: 15px;
  transition: all 0.3s ease;
}

.philosophy-item:hover {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  transform: translateY(-3px);
}

.philosophy-icon {
  font-size: 1.8rem;
  width: 50px;
  height: 50px;
  background: white;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.philosophy-content h4 {
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.philosophy-content p {
  font-size: 0.85rem;
  opacity: 0.8;
  margin: 0;
  line-height: 1.4;
}

@media (max-width: 1024px) {
  .about-wrapper {
    grid-template-columns: 1fr;
    gap: 3rem;
  }

  .philosophy-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .about {
    padding: 4rem 0;
  }

  .container {
    padding: 0 1rem;
  }

  .profile-section,
  .bio-section,
  .skills-section,
  .philosophy-section {
    padding: 2rem;
  }

  .profile-avatar {
    width: 100px;
    height: 100px;
    font-size: 2.5rem;
  }

  .profile-name {
    font-size: 1.8rem;
  }
}
</style>
