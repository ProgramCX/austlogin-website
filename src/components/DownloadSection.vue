<template>
  <section id="download" class="section">
    <div class="container">
      <h2 class="section-title">下载安装</h2>
      <p class="section-subtitle">
        选择适合您的下载方式，开始体验便捷的校园网连接
      </p>
      
      <div class="download-cards">
        <!-- 最新版本下载 -->
        <div class="download-card download-card-primary">
          <div class="download-card-header">
            <div class="version-badge">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2" />
              </svg>
              推荐
            </div>
            <h3 class="download-card-title">最新版本</h3>
            <p class="download-card-version">v0.1.0-alpha</p>
          </div>
          
          <div class="download-card-content">
            <ul class="download-features">
              <li>
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                一键登录校园网
              </li>
              <li>
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                自动登录功能
              </li>
              <li>
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Material You 设计
              </li>
              <li>
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                多 ISP 通道支持
              </li>
            </ul>
          </div>
          
          <div class="download-card-footer">
            <a :href="latestDownloadUrl" class="btn btn-primary btn-lg download-btn" download>
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/>
                <polyline points="7 10 12 15 17 10"/>
                <line x1="12" y1="15" x2="12" y2="3"/>
              </svg>
              立即下载 APK
            </a>
            <p class="download-size">大小: ~5MB · 需要 Android 8.0+</p>
          </div>
        </div>
        
        <!-- 历史版本 -->
        <div class="download-card">
          <div class="download-card-header">
            <div class="history-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <circle cx="12" cy="12" r="10"/>
                <polyline points="12 6 12 12 16 14"/>
              </svg>
            </div>
            <h3 class="download-card-title">历史版本</h3>
            <p class="download-card-desc">查看所有发布版本</p>
          </div>
          
          <div class="download-card-content">
            <p class="history-description">
              访问 GitHub Releases 页面查看所有历史版本，包括更新日志、变更记录和下载链接。
            </p>
            
            <div class="github-info">
              <div class="github-stat">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/>
                </svg>
                <span>开源项目</span>
              </div>
              <div class="github-stat">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>
                </svg>
                <span>MIT 协议</span>
              </div>
            </div>
          </div>
          
          <div class="download-card-footer">
            <a 
              href="https://github.com/ProgramCX/AUSTLogin/releases" 
              target="_blank" 
              class="btn btn-secondary btn-lg download-btn"
            >
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
              前往 GitHub Releases
            </a>
          </div>
        </div>
      </div>
      
      <!-- 安装说明 -->
      <div class="install-guide">
        <h3 class="install-title">安装说明</h3>
        <div class="install-steps">
          <div class="install-step">
            <div class="step-number">1</div>
            <div class="step-content">
              <h4>下载 APK</h4>
              <p>点击上方下载按钮获取安装包</p>
            </div>
          </div>
          <div class="install-step">
            <div class="step-number">2</div>
            <div class="step-content">
              <h4>允许安装</h4>
              <p>在设置中允许安装未知来源应用</p>
            </div>
          </div>
          <div class="install-step">
            <div class="step-number">3</div>
            <div class="step-content">
              <h4>安装应用</h4>
              <p>打开下载的 APK 文件进行安装</p>
            </div>
          </div>
          <div class="install-step">
            <div class="step-number">4</div>
            <div class="step-content">
              <h4>开始使用</h4>
              <p>输入账号密码即可登录校园网</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// 最新版本下载链接 - 可自定义修改
const latestDownloadUrl = ref('https://github.com/ProgramCX/AUSTLogin/releases/latest/download/austlogin-0.1.0-alpha.apk')
</script>

<style scoped>
.download-cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--space-xl);
  max-width: 900px;
  margin: 0 auto var(--space-3xl);
}

.download-card {
  background: var(--bg-primary);
  border-radius: var(--radius-2xl);
  padding: var(--space-2xl);
  border: 1px solid var(--border-color);
  display: flex;
  flex-direction: column;
  transition: all var(--transition-normal);
}

.download-card:hover {
  box-shadow: var(--shadow-xl);
  transform: translateY(-4px);
}

.download-card-primary {
  background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
  border-color: rgba(99, 102, 241, 0.2);
}

.download-card-header {
  text-align: center;
  margin-bottom: var(--space-xl);
}

.version-badge {
  display: inline-flex;
  align-items: center;
  gap: var(--space-xs);
  padding: var(--space-xs) var(--space-md);
  background: var(--primary-gradient);
  color: white;
  border-radius: var(--radius-2xl);
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: var(--space-md);
}

.version-badge svg {
  width: 14px;
  height: 14px;
}

.history-icon {
  width: 56px;
  height: 56px;
  margin: 0 auto var(--space-md);
  background: var(--bg-tertiary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-secondary);
}

.history-icon svg {
  width: 28px;
  height: 28px;
}

.download-card-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: var(--space-xs);
}

.download-card-version {
  font-size: 1.125rem;
  color: var(--primary-color);
  font-weight: 600;
}

.download-card-desc {
  color: var(--text-secondary);
}

.download-card-content {
  flex: 1;
  margin-bottom: var(--space-xl);
}

.download-features {
  display: flex;
  flex-direction: column;
  gap: var(--space-md);
}

.download-features li {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  font-size: 0.9375rem;
  color: var(--text-secondary);
}

.download-features svg {
  width: 20px;
  height: 20px;
  color: var(--success-color);
  flex-shrink: 0;
}

.history-description {
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: var(--space-xl);
}

.github-info {
  display: flex;
  gap: var(--space-xl);
}

.github-stat {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  color: var(--text-tertiary);
  font-size: 0.875rem;
}

.github-stat svg {
  width: 18px;
  height: 18px;
}

.download-card-footer {
  text-align: center;
}

.download-btn {
  width: 100%;
  justify-content: center;
}

.download-btn svg {
  width: 20px;
  height: 20px;
}

.download-size {
  margin-top: var(--space-sm);
  font-size: 0.875rem;
  color: var(--text-tertiary);
}

/* 安装说明 */
.install-guide {
  max-width: 800px;
  margin: 0 auto;
  padding: var(--space-2xl);
  background: var(--bg-secondary);
  border-radius: var(--radius-2xl);
}

.install-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text-primary);
  text-align: center;
  margin-bottom: var(--space-xl);
}

.install-steps {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: var(--space-lg);
}

.install-step {
  text-align: center;
}

.step-number {
  width: 40px;
  height: 40px;
  margin: 0 auto var(--space-md);
  background: var(--primary-gradient);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.125rem;
  font-weight: 700;
}

.step-content h4 {
  font-size: 0.9375rem;
  font-weight: 600;
  color: var(--text-primary);
  margin-bottom: var(--space-xs);
}

.step-content p {
  font-size: 0.875rem;
  color: var(--text-secondary);
}

@media (max-width: 768px) {
  .download-cards {
    grid-template-columns: 1fr;
  }
  
  .install-steps {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--space-xl);
  }
}

@media (max-width: 480px) {
  .install-steps {
    grid-template-columns: 1fr;
  }
  
  .download-card {
    padding: var(--space-xl);
  }
}
</style>
