<template>
  <section id="contact" class="contact">
    <div class="container">
      <h2 class="section-title">Contact</h2>
      <div class="contact-content">
        <div class="contact-info">
          <h3>연락 주세요!</h3>
          <p>
            새로운 프로젝트나 협업 기회에 대해 이야기하고 싶습니다. 언제든지
            연락주시면 빠른 시간 내에 답변드리겠습니다.
          </p>
          <div class="contact-methods">
            <div class="contact-method">
              <div class="contact-icon">📧</div>
              <div class="contact-details">
                <h4>Email</h4>
                <a href="mailto:developer@example.com">developer@example.com</a>
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-icon">📱</div>
              <div class="contact-details">
                <h4>Phone</h4>
                <a href="tel:+821012345678">010-1234-5678</a>
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-icon">💼</div>
              <div class="contact-details">
                <h4>LinkedIn</h4>
                <a href="https://linkedin.com/in/developer" target="_blank"
                  >linkedin.com/in/developer</a
                >
              </div>
            </div>
            <div class="contact-method">
              <div class="contact-icon">🐙</div>
              <div class="contact-details">
                <h4>GitHub</h4>
                <a href="https://github.com/developer" target="_blank"
                  >github.com/developer</a
                >
              </div>
            </div>
          </div>
        </div>
        <div class="contact-form">
          <form @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">이름</label>
              <input
                type="text"
                id="name"
                v-model="form.name"
                required
                placeholder="이름을 입력하세요"
              />
            </div>
            <div class="form-group">
              <label for="email">이메일</label>
              <input
                type="email"
                id="email"
                v-model="form.email"
                required
                placeholder="이메일을 입력하세요"
              />
            </div>
            <div class="form-group">
              <label for="subject">제목</label>
              <input
                type="text"
                id="subject"
                v-model="form.subject"
                required
                placeholder="메시지 제목을 입력하세요"
              />
            </div>
            <div class="form-group">
              <label for="message">메시지</label>
              <textarea
                id="message"
                v-model="form.message"
                required
                rows="5"
                placeholder="메시지를 입력하세요"
              ></textarea>
            </div>
            <button type="submit" class="submit-btn" :disabled="isSubmitting">
              {{ isSubmitting ? "전송 중..." : "메시지 보내기" }}
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const isSubmitting = ref(false);

const form = ref({
  name: "",
  email: "",
  subject: "",
  message: "",
});

const submitForm = async () => {
  isSubmitting.value = true;

  // 실제 구현에서는 여기서 API 호출을 합니다
  setTimeout(() => {
    alert("메시지가 성공적으로 전송되었습니다!");
    form.value = { name: "", email: "", subject: "", message: "" };
    isSubmitting.value = false;
  }, 2000);
};
</script>

<style scoped>
.contact {
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

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.contact-info h3 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
  color: #333;
}

.contact-info p {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #666;
  margin-bottom: 2rem;
}

.contact-methods {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-method {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background: #f8f9fa;
  border-radius: 10px;
  transition: transform 0.3s ease;
}

.contact-method:hover {
  transform: translateX(5px);
}

.contact-icon {
  font-size: 2rem;
  width: 60px;
  text-align: center;
}

.contact-details h4 {
  margin: 0 0 0.25rem 0;
  color: #333;
  font-weight: 600;
}

.contact-details a {
  color: #667eea;
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-details a:hover {
  color: #764ba2;
}

.contact-form {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 600;
  color: #333;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.75rem;
  border: 2px solid #e0e0e0;
  border-radius: 8px;
  font-size: 1rem;
  transition: border-color 0.3s ease;
  box-sizing: border-box;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #667eea;
}

.submit-btn {
  width: 100%;
  padding: 1rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.submit-btn:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
}

.submit-btn:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .contact-form {
    padding: 1.5rem;
  }
}
</style>
