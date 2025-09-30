<template>
  <nav class="navigation" :class="{ scrolled: isScrolled }">
    <div class="nav-container">
      <div class="nav-logo">
        <a href="#hero">이하영</a>
      </div>
      <div class="nav-menu" :class="{ active: isMenuOpen }">
        <a href="#about" @click="closeMenu">About</a>
        <a href="#skills" @click="closeMenu">Skills</a>
        <a href="#projects" @click="closeMenu">Projects</a>
        <a href="#contact" @click="closeMenu">Contact</a>
      </div>
      <div class="nav-toggle" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from "vue";

const isScrolled = ref(false);
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};

// 스크롤 이벤트 리스너
window.addEventListener("scroll", () => {
  isScrolled.value = window.scrollY > 100;
});
</script>

<style scoped>
.navigation {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  z-index: 1000;
  transition: background-color 0.3s ease;
}

.navigation.scrolled {
  background-color: rgba(255, 255, 255, 1);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.nav-logo a {
  font-size: 1.8rem;
  font-weight: 700;
  color: #333;
  text-decoration: none;
  transition: color 0.3s ease;
}

.nav-logo a:hover {
  color: #667eea;
}

.nav-menu {
  display: flex;
  gap: 2rem;
  align-items: center;
}

.nav-menu a {
  font-size: 1rem;
  font-weight: 500;
  color: #333;
  text-decoration: none;
  transition: color 0.3s ease;
}

.nav-menu a:hover {
  color: #667eea;
}

.nav-toggle {
  display: none; /* 모바일 메뉴 토글 버튼 */
  flex-direction: column;
  justify-content: space-around;
  width: 30px;
  height: 21px;
  cursor: pointer;
  z-index: 1001;
}

.nav-toggle span {
  display: block;
  width: 100%;
  height: 3px;
  background-color: #333;
  border-radius: 2px;
  transition: all 0.3s ease;
}

.nav-toggle.active span:nth-child(1) {
  transform: translateY(11px) rotate(45deg);
}

.nav-toggle.active span:nth-child(2) {
  opacity: 0;
}

.nav-toggle.active span:nth-child(3) {
  transform: translateY(-11px) rotate(-45deg);
}

@media (max-width: 768px) {
  .nav-menu {
    position: fixed;
    top: 0;
    right: -100%; /* 메뉴 숨김 */
    width: 70%;
    height: 100vh;
    background-color: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(15px);
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: right 0.5s ease-in-out;
    z-index: 999;
    padding: 2rem;
    box-shadow: -5px 0 10px rgba(0, 0, 0, 0.1);
  }

  .nav-menu.active {
    right: 0; /* 메뉴 표시 */
  }

  .nav-menu a {
    font-size: 1.2rem;
    margin-bottom: 1.5rem;
  }

  .nav-toggle {
    display: flex; /* 모바일 메뉴 토글 버튼 표시 */
  }
}
</style>
