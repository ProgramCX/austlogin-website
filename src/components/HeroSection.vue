<template>
  <section class="hero bg-gradient-radial">
    <div class="container hero-content">
      <div class="hero-text">
        <div class="hero-badge badge badge-primary">
          <svg class="badge-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          v0.1.0-alpha · 最新版本
        </div>
        
        <h1 class="hero-title">
          快接安理大校园网
          <span class="hero-title-sub">校园网自动登录</span>
        </h1>
        
        <p class="hero-description">
          专为安徽理工大学校园网设计的自动登录工具，连接 WiFi 即自动认证，
          告别繁琐的网页登录流程，让校园网连接更轻松。
        </p>
        
        <div class="hero-actions">
          <a href="#download" class="btn btn-primary btn-lg">
            <svg class="btn-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/>
              <polyline points="7 10 12 15 17 10"/>
              <line x1="12" y1="15" x2="12" y2="3"/>
            </svg>
            立即下载
          </a>
          <a 
            href="https://github.com/ProgramCX/AUSTLogin" 
            target="_blank" 
            class="btn btn-secondary btn-lg"
          >
            <svg class="btn-icon" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
            查看源码
          </a>
        </div>
        
        <div class="hero-stats">
          <div class="stat">
            <span class="stat-value">Android 8+</span>
            <span class="stat-label">系统要求</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-value">Material 3</span>
            <span class="stat-label">设计风格</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-value">MIT</span>
            <span class="stat-label">开源协议</span>
          </div>
        </div>
      </div>
      
      <div class="hero-visual">
        <div class="phone-mockup animate-float">
          <img src="/screenshots/1.png" alt="App Screenshot" class="phone-screen" />
        </div>
        <div class="hero-glow"></div>
      </div>
    </div>
    
    <div class="hero-wave">
      <svg viewBox="0 0 1440 120" fill="none" preserveAspectRatio="none">
        <path d="M0 120L60 105C120 90 240 60 360 45C480 30 600 30 720 37.5C840 45 960 60 1080 67.5C1200 75 1320 75 1380 75L1440 75V120H1380C1320 120 1200 120 1080 120C960 120 840 120 720 120C600 120 480 120 360 120C240 120 120 120 60 120H0Z" fill="white"/>
      </svg>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  position: relative;
  padding-top: 120px;
  padding-bottom: 80px;
  overflow: hidden;
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--space-3xl);
  align-items: center;
}

.hero-badge {
  margin-bottom: var(--space-lg);
}

.badge-icon {
  width: 16px;
  height: 16px;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: var(--space-lg);
  color: var(--text-primary);
}

.hero-title-sub {
  display: block;
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-description {
  font-size: 1.25rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: var(--space-xl);
  max-width: 500px;
}

.hero-actions {
  display: flex;
  gap: var(--space-md);
  margin-bottom: var(--space-2xl);
  flex-wrap: wrap;
}

.btn-icon {
  width: 20px;
  height: 20px;
}

.hero-stats {
  display: flex;
  align-items: center;
  gap: var(--space-xl);
}

.stat {
  display: flex;
  flex-direction: column;
  gap: var(--space-xs);
}

.stat-value {
  font-size: 1.125rem;
  font-weight: 700;
  color: var(--text-primary);
}

.stat-label {
  font-size: 0.875rem;
  color: var(--text-tertiary);
}

.stat-divider {
  width: 1px;
  height: 40px;
  background: var(--border-color);
}

.hero-visual {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.phone-mockup {
  position: relative;
  width: 280px;
  padding: 12px;
  background: linear-gradient(145deg, #1a1a2e 0%, #16213e 100%);
  border-radius: 40px;
  box-shadow: var(--shadow-xl), 0 30px 60px -15px rgba(0, 0, 0, 0.3);
}

.phone-screen {
  width: 100%;
  border-radius: 28px;
}

.hero-glow {
  position: absolute;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.2) 0%, transparent 70%);
  z-index: -1;
}

.hero-wave {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 120px;
}

.hero-wave svg {
  width: 100%;
  height: 100%;
}

@media (max-width: 968px) {
  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-description {
    margin-left: auto;
    margin-right: auto;
  }
  
  .hero-actions {
    justify-content: center;
  }
  
  .hero-stats {
    justify-content: center;
  }
  
  .hero-visual {
    order: -1;
    margin-bottom: var(--space-xl);
  }
  
  .phone-mockup {
    width: 220px;
  }
}

@media (max-width: 480px) {
  .hero-title {
    font-size: 2rem;
  }
  
  .hero-description {
    font-size: 1rem;
  }
  
  .hero-stats {
    flex-direction: column;
    gap: var(--space-md);
  }
  
  .stat-divider {
    display: none;
  }
  
  .hero-actions {
    flex-direction: column;
    align-items: stretch;
  }
}
</style>
