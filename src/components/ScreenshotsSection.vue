<template>
  <section id="screenshots" class="section bg-gradient">
    <div class="container">
      <h2 class="section-title">应用截图</h2>
      <p class="section-subtitle">
        精美的 Material You 界面设计，给您最佳的视觉体验
      </p>
      
      <div class="carousel-wrapper">
        <button 
          class="carousel-btn carousel-btn-prev" 
          @click="prevSlide"
          :disabled="currentIndex === 0"
        >
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polyline points="15 18 9 12 15 6" />
          </svg>
        </button>
        
        <div class="carousel-container">
          <div 
            class="carousel-track" 
            :style="{ transform: `translateX(-${currentIndex * slideWidth}%)` }"
          >
            <div 
              v-for="(screenshot, index) in screenshots" 
              :key="index"
              class="carousel-slide"
              :class="{ 'active': index === currentIndex }"
            >
              <div class="phone-frame">
                <img :src="screenshot.src" :alt="screenshot.alt" class="screenshot-img" />
              </div>
              <p class="screenshot-caption">{{ screenshot.caption }}</p>
            </div>
          </div>
        </div>
        
        <button 
          class="carousel-btn carousel-btn-next" 
          @click="nextSlide"
          :disabled="currentIndex === screenshots.length - 1"
        >
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polyline points="9 18 15 12 9 6" />
          </svg>
        </button>
      </div>
      
      <div class="carousel-dots">
        <button 
          v-for="(_, index) in screenshots" 
          :key="index"
          class="carousel-dot"
          :class="{ 'active': index === currentIndex }"
          @click="goToSlide(index)"
        />
      </div>
      
      <!-- 缩略图预览 -->
      <div class="thumbnails">
        <button 
          v-for="(screenshot, index) in screenshots" 
          :key="index"
          class="thumbnail"
          :class="{ 'active': index === currentIndex }"
          @click="goToSlide(index)"
        >
          <img :src="screenshot.src" :alt="screenshot.alt" />
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

const screenshots = [
  { src: '/screenshots/1.png', alt: '主界面', caption: '简洁的登录主界面' },
  { src: '/screenshots/2.jpg', alt: '设置页面', caption: '丰富的个性化设置' },
  { src: '/screenshots/3.jpg', alt: '自动登录', caption: '智能自动登录功能' },
  { src: '/screenshots/4.jpg', alt: '登录日志', caption: '详细的登录日志记录' }
]

const currentIndex = ref(0)
const slideWidth = computed(() => 100)

let autoPlayTimer = null

const nextSlide = () => {
  if (currentIndex.value < screenshots.length - 1) {
    currentIndex.value++
  } else {
    currentIndex.value = 0
  }
}

const prevSlide = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--
  } else {
    currentIndex.value = screenshots.length - 1
  }
}

const goToSlide = (index) => {
  currentIndex.value = index
}

const startAutoPlay = () => {
  autoPlayTimer = setInterval(() => {
    nextSlide()
  }, 4000)
}

const stopAutoPlay = () => {
  if (autoPlayTimer) {
    clearInterval(autoPlayTimer)
  }
}

onMounted(() => {
  startAutoPlay()
})

onUnmounted(() => {
  stopAutoPlay()
})
</script>

<style scoped>
.carousel-wrapper {
  position: relative;
  display: flex;
  align-items: center;
  gap: var(--space-lg);
  max-width: 600px;
  margin: 0 auto;
}

.carousel-container {
  flex: 1;
  overflow: hidden;
  border-radius: var(--radius-xl);
}

.carousel-track {
  display: flex;
  transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

.carousel-slide {
  flex: 0 0 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 var(--space-md);
  opacity: 0.5;
  transform: scale(0.9);
  transition: all 0.5s ease;
}

.carousel-slide.active {
  opacity: 1;
  transform: scale(1);
}

.phone-frame {
  background: linear-gradient(145deg, #1a1a2e 0%, #16213e 100%);
  padding: 12px;
  border-radius: 36px;
  box-shadow: var(--shadow-xl), 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

.screenshot-img {
  width: 260px;
  border-radius: 24px;
  display: block;
}

.screenshot-caption {
  margin-top: var(--space-lg);
  font-size: 1rem;
  color: var(--text-secondary);
  font-weight: 500;
}

.carousel-btn {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: var(--bg-primary);
  border: 1px solid var(--border-color);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-primary);
  transition: all var(--transition-normal);
  flex-shrink: 0;
}

.carousel-btn:hover:not(:disabled) {
  background: var(--primary-color);
  border-color: var(--primary-color);
  color: white;
  transform: scale(1.05);
}

.carousel-btn:disabled {
  opacity: 0.3;
  cursor: not-allowed;
}

.carousel-btn svg {
  width: 24px;
  height: 24px;
}

.carousel-dots {
  display: flex;
  justify-content: center;
  gap: var(--space-sm);
  margin-top: var(--space-xl);
}

.carousel-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: var(--border-color);
  transition: all var(--transition-normal);
}

.carousel-dot.active {
  background: var(--primary-color);
  transform: scale(1.2);
}

.carousel-dot:hover:not(.active) {
  background: var(--text-tertiary);
}

.thumbnails {
  display: flex;
  justify-content: center;
  gap: var(--space-md);
  margin-top: var(--space-xl);
  flex-wrap: wrap;
}

.thumbnail {
  width: 80px;
  height: auto;
  border-radius: var(--radius-md);
  overflow: hidden;
  border: 3px solid transparent;
  transition: all var(--transition-normal);
  opacity: 0.6;
}

.thumbnail.active {
  border-color: var(--primary-color);
  opacity: 1;
  transform: scale(1.05);
}

.thumbnail:hover:not(.active) {
  opacity: 0.9;
}

.thumbnail img {
  width: 100%;
  height: auto;
  display: block;
}

@media (max-width: 768px) {
  .carousel-btn {
    width: 40px;
    height: 40px;
  }
  
  .carousel-btn svg {
    width: 20px;
    height: 20px;
  }
  
  .screenshot-img {
    width: 220px;
  }
  
  .phone-frame {
    padding: 10px;
    border-radius: 30px;
  }
  
  .thumbnail {
    width: 60px;
  }
}

@media (max-width: 480px) {
  .carousel-wrapper {
    gap: var(--space-sm);
  }
  
  .carousel-btn {
    width: 36px;
    height: 36px;
  }
  
  .screenshot-img {
    width: 180px;
  }
}
</style>
