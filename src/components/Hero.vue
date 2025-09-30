<template>
  <section id="hero" class="hero">
    <div class="hero-background">
      <div class="floating-shapes">
        <div class="shape shape-1"></div>
        <div class="shape shape-2"></div>
        <div class="shape shape-3"></div>
        <div class="shape shape-4"></div>
      </div>
    </div>
    <div class="hero-content">
      <div class="hero-text">
        <div class="greeting">안녕하세요 👋</div>
        <h1 class="hero-title"><span class="highlight">이하영</span>입니다</h1>
        <div class="typing-animation">
          <span class="typing-text">{{ currentText }}</span>
          <span class="cursor">|</span>
        </div>
        <p class="hero-description">
          창의적이고 혁신적인 웹 애플리케이션을 개발하는<br />
          <strong>풀스택 개발자</strong>입니다. 사용자 경험을 최우선으로
          생각하며<br />
          최신 기술 트렌드를 활용한 솔루션을 제공합니다.
        </p>

        <div class="social-links">
          <a href="#" class="social-link btn btn-primary">GitHub</a>
          <a href="#" class="social-link btn btn-primary">LinkedIn</a>
          <a href="#" class="social-link btn btn-primary">Email</a>
        </div>
      </div>
      <div class="hero-image">
        <div class="profile-container">
          <div class="profile-ring"></div>
          <div class="profile-image">
            <div class="profile-icon">🧑‍💻</div>
          </div>
          <div class="floating-icons">
            <div class="icon icon-1">⚡</div>
            <div class="icon icon-2">🚀</div>
            <div class="icon icon-3">💡</div>
            <div class="icon icon-4">🎯</div>
          </div>
        </div>
      </div>
    </div>
    <div class="scroll-indicator">
      <div class="scroll-arrow"></div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const currentText = ref("");
const texts = ["풀스택 개발자", "프론트엔드 개발자", "백엔드 개발자"];
let textIndex = 0;
let charIndex = 0;
let isDeleting = false;

const typeWriter = () => {
  const fullText = texts[textIndex];

  if (isDeleting) {
    currentText.value = fullText.substring(0, charIndex - 1);
    charIndex--;
  } else {
    currentText.value = fullText.substring(0, charIndex + 1);
    charIndex++;
  }

  let typeSpeed = isDeleting ? 50 : 100;

  if (!isDeleting && charIndex === fullText.length) {
    typeSpeed = 2000;
    isDeleting = true;
  } else if (isDeleting && charIndex === 0) {
    isDeleting = false;
    textIndex = (textIndex + 1) % texts.length;
    typeSpeed = 500;
  }

  setTimeout(typeWriter, typeSpeed);
};

onMounted(() => {
  typeWriter();
});
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  overflow: hidden;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.floating-shapes {
  position: absolute;
  width: 100%;
  height: 100%;
}

.shape {
  position: absolute;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  animation: float 6s ease-in-out infinite;
}

.shape-1 {
  width: 80px;
  height: 80px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 120px;
  height: 120px;
  top: 60%;
  right: 10%;
  animation-delay: 2s;
}

.shape-3 {
  width: 60px;
  height: 60px;
  top: 80%;
  left: 20%;
  animation-delay: 4s;
}

.shape-4 {
  width: 100px;
  height: 100px;
  top: 30%;
  right: 30%;
  animation-delay: 1s;
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(180deg);
  }
}

.hero-content {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6rem;
  align-items: center;
  position: relative;
  z-index: 2;
}

.hero-text {
  color: white;
}

.greeting {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 1rem;
  opacity: 0.9;
  animation: slideInLeft 1s ease-out;
}

.hero-title {
  font-size: 4rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  line-height: 1.1;
  animation: slideInLeft 1s ease-out 0.2s both;
}

.highlight {
  background: linear-gradient(45deg, #ffd700, #ffed4e, #ffd700);
  background-size: 200% 200%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradientShift 3s ease-in-out infinite;
}

@keyframes gradientShift {
  0%,
  100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

.typing-animation {
  font-size: 1.8rem;
  font-weight: 600;
  margin-bottom: 2rem;
  min-height: 2.5rem;
  animation: slideInLeft 1s ease-out 0.4s both;
}

.typing-text {
  color: #ffd700;
}

.cursor {
  animation: blink 1s infinite;
  color: #ffd700;
}

@keyframes blink {
  0%,
  50% {
    opacity: 1;
  }
  51%,
  100% {
    opacity: 0;
  }
}

.hero-description {
  font-size: 1.2rem;
  line-height: 1.8;
  margin-bottom: 3rem;
  opacity: 0.95;
  animation: slideInLeft 1s ease-out 0.6s both;
}

.hero-buttons {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 3rem;
  animation: slideInLeft 1s ease-out 0.8s both;
}

.btn {
  position: relative;
  padding: 0.2rem 1rem;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  overflow: hidden;
  border: none;
  cursor: pointer;
}

.btn span {
  position: relative;
  z-index: 2;
}

.btn-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 50px;
  transition: all 0.3s ease;
}

.btn-primary {
  background: linear-gradient(45deg, #ffd700, #ffed4e);
  color: #333;
  box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(255, 215, 0, 0.6);
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid rgba(255, 255, 255, 0.8);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: white;
  transform: translateY(-3px);
}

.social-links {
  display: flex;
  gap: 1rem;
  animation: slideInLeft 1s ease-out 1s both;
}

.social-link {
  color: rgba(255, 255, 255, 0.8);
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
  position: relative;
}

.social-link:hover {
  color: #ffd700;
  transform: translateY(-2px);
}

.social-link::after {
  content: "";
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #ffd700;
  transition: width 0.3s ease;
}

.social-link:hover::after {
  width: 100%;
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
  animation: slideInRight 1s ease-out 0.5s both;
}

.profile-container {
  position: relative;
  width: 400px;
  height: 400px;
}

.profile-ring {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  border: 3px solid rgba(255, 215, 0, 0.3);
  border-radius: 50%;
  animation: rotate 20s linear infinite;
}

.profile-ring::before {
  content: "";
  position: absolute;
  top: -3px;
  left: 50%;
  width: 20px;
  height: 20px;
  background: #ffd700;
  border-radius: 50%;
  transform: translateX(-50%);
}

@keyframes rotate {
  from {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  to {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}

.profile-image {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  height: 300px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(20px);
  border: 2px solid rgba(255, 255, 255, 0.2);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.profile-icon {
  font-size: 8rem;
  filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.5));
}

.floating-icons {
  position: absolute;
  width: 100%;
  height: 100%;
}

.icon {
  position: absolute;
  font-size: 2rem;
  animation: floatIcon 4s ease-in-out infinite;
}

.icon-1 {
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.icon-2 {
  top: 10%;
  right: 10%;
  animation-delay: 1s;
}

.icon-3 {
  bottom: 10%;
  left: 10%;
  animation-delay: 2s;
}

.icon-4 {
  bottom: 10%;
  right: 10%;
  animation-delay: 3s;
}

@keyframes floatIcon {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-15px);
  }
}

.scroll-indicator {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
}

.scroll-arrow {
  width: 30px;
  height: 30px;
  border: 2px solid rgba(255, 255, 255, 0.8);
  border-top: none;
  border-left: none;
  transform: rotate(45deg);
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0) rotate(45deg);
  }
  40% {
    transform: translateY(-10px) rotate(45deg);
  }
  60% {
    transform: translateY(-5px) rotate(45deg);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 768px) {
  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 3rem;
    padding: 0 1rem;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .typing-animation {
    font-size: 1.4rem;
  }

  .hero-description {
    font-size: 1.1rem;
  }

  .hero-buttons {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }

  .btn {
    width: 200px;
  }

  .profile-container {
    width: 250px;
    height: 250px;
  }

  .profile-image {
    width: 200px;
    height: 200px;
  }

  .profile-icon {
    font-size: 5rem;
  }

  .social-links {
    justify-content: center;
  }
}
</style>
