<template>
  <section id="tech" class="section bg-gradient">
    <div class="container">
      <h2 class="section-title">技术栈</h2>
      <p class="section-subtitle">
        采用现代化的 Android 开发技术，确保应用的性能与可维护性
      </p>
      
      <div class="tech-grid">
        <div v-for="tech in technologies" :key="tech.name" class="tech-card">
          <div class="tech-icon" :style="{ background: tech.color }">
            {{ tech.icon }}
          </div>
          <div class="tech-info">
            <h3 class="tech-name">{{ tech.name }}</h3>
            <p class="tech-desc">{{ tech.description }}</p>
          </div>
        </div>
      </div>
      
      <!-- ISP 通道说明 -->
      <div class="isp-section">
        <h3 class="isp-title">支持的 ISP 通道</h3>
        <div class="isp-grid">
          <div v-for="isp in ispChannels" :key="isp.name" class="isp-card">
            <div class="isp-icon" :style="{ background: isp.color }">
              {{ isp.icon }}
            </div>
            <div class="isp-info">
              <h4 class="isp-name">{{ isp.name }}</h4>
              <p class="isp-desc">{{ isp.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const technologies = [
  {
    name: 'Kotlin',
    description: '现代化的 Android 开发语言，简洁安全',
    icon: 'K',
    color: 'linear-gradient(135deg, #7F52FF 0%, #C711E1 100%)'
  },
  {
    name: 'Jetpack Compose',
    description: '声明式 UI 框架，构建原生界面',
    icon: '🎨',
    color: 'linear-gradient(135deg, #4285F4 0%, #34A853 100%)'
  },
  {
    name: 'Material Design 3',
    description: 'Google 最新设计规范，支持动态主题',
    icon: 'M3',
    color: 'linear-gradient(135deg, #6750A4 0%, #B3261E 100%)'
  },
  {
    name: 'MVVM 架构',
    description: '清晰的代码架构，易于维护扩展',
    icon: '🏗️',
    color: 'linear-gradient(135deg, #FF6B6B 0%, #FFE66D 100%)'
  },
  {
    name: 'Kotlin Coroutines',
    description: '优雅的异步编程，流畅的用户体验',
    icon: '⚡',
    color: 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)'
  },
  {
    name: 'DataStore',
    description: '现代化数据存储，替代 SharedPreferences',
    icon: '💾',
    color: 'linear-gradient(135deg, #11998e 0%, #38ef7d 100%)'
  }
]

const ispChannels = [
  {
    name: '校内免费资源',
    description: '使用校园局域网出口，适合校内资源访问',
    icon: '🏫',
    color: 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)'
  },
  {
    name: '中国移动',
    description: '使用移动宽带出口',
    icon: '📱',
    color: 'linear-gradient(135deg, #11998e 0%, #38ef7d 100%)'
  },
  {
    name: '中国联通',
    description: '使用联通宽带出口',
    icon: '📶',
    color: 'linear-gradient(135deg, #e52d27 0%, #b31217 100%)'
  },
  {
    name: '中国电信',
    description: '使用电信宽带出口',
    icon: '🌐',
    color: 'linear-gradient(135deg, #2193b0 0%, #6dd5ed 100%)'
  }
]
</script>

<style scoped>
.tech-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--space-lg);
  margin-bottom: var(--space-3xl);
}

.tech-card {
  display: flex;
  align-items: center;
  gap: var(--space-md);
  padding: var(--space-lg);
  background: var(--bg-primary);
  border-radius: var(--radius-xl);
  border: 1px solid var(--border-color);
  transition: all var(--transition-normal);
}

.tech-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

.tech-icon {
  width: 56px;
  height: 56px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.25rem;
  font-weight: 700;
  color: white;
  flex-shrink: 0;
}

.tech-info {
  flex: 1;
}

.tech-name {
  font-size: 1rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: var(--space-xs);
}

.tech-desc {
  font-size: 0.875rem;
  color: var(--text-secondary);
}

/* ISP 通道 */
.isp-section {
  max-width: 800px;
  margin: 0 auto;
}

.isp-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text-primary);
  text-align: center;
  margin-bottom: var(--space-xl);
}

.isp-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--space-md);
}

.isp-card {
  display: flex;
  align-items: center;
  gap: var(--space-md);
  padding: var(--space-md) var(--space-lg);
  background: var(--bg-primary);
  border-radius: var(--radius-lg);
  border: 1px solid var(--border-color);
}

.isp-icon {
  width: 44px;
  height: 44px;
  border-radius: var(--radius-md);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.25rem;
  flex-shrink: 0;
}

.isp-name {
  font-size: 0.9375rem;
  font-weight: 600;
  color: var(--text-primary);
  margin-bottom: 2px;
}

.isp-desc {
  font-size: 0.8125rem;
  color: var(--text-secondary);
}

@media (max-width: 1024px) {
  .tech-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .tech-grid {
    grid-template-columns: 1fr;
  }
  
  .isp-grid {
    grid-template-columns: 1fr;
  }
}
</style>
