<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-brand">
          <a href="#" class="footer-logo">
            <img src="/logo.png" alt="Logo" class="footer-logo-img" />
            <span class="footer-logo-text">快接安理大校园网</span>
          </a>
          <p class="footer-tagline">
            专为安徽理工大学校园网设计的自动登录工具
          </p>
        </div>
        
        <div class="footer-links">
          <div class="footer-column">
            <h4 class="footer-column-title">产品</h4>
            <ul class="footer-list">
              <li><a href="#features">功能特性</a></li>
              <li><a href="#screenshots">应用截图</a></li>
              <li><a href="#download">下载安装</a></li>
              <li><a href="#tech">技术栈</a></li>
            </ul>
          </div>
          
          <div class="footer-column">
            <h4 class="footer-column-title">开源</h4>
            <ul class="footer-list">
              <li>
                <a href="https://github.com/ProgramCX/AUSTLogin" target="_blank">
                  GitHub 仓库
                </a>
              </li>
              <li>
                <a href="https://github.com/ProgramCX/AUSTLogin/releases" target="_blank">
                  版本发布
                </a>
              </li>
              <li>
                <a href="https://github.com/ProgramCX/AUSTLogin/issues" target="_blank">
                  问题反馈
                </a>
              </li>
              <li>
                <a href="https://github.com/ProgramCX/AUSTLogin/blob/main/LICENSE" target="_blank">
                  MIT 协议
                </a>
              </li>
            </ul>
          </div>
          
          <div class="footer-column">
            <h4 class="footer-column-title">联系我们</h4>
            <ul class="footer-list">
              <li>
                <a href="https://github.com/ProgramCX" target="_blank">
                  开发者主页
                </a>
              </li>
              <li>
                <a href="https://github.com/ProgramCX/AUSTLogin/issues/new" target="_blank">
                  提交 Issue
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="footer-bottom">
        <div class="footer-copyright">
          <p>© {{ currentYear }} 快接安理大校园网. 基于 MIT 协议开源.</p>
        </div>
        
        <div class="footer-legal">
          <a href="#" class="legal-link">隐私政策</a>
          <span class="legal-divider">|</span>
          <a href="#" class="legal-link">用户协议</a>
          <span class="legal-divider">|</span>
          <a href="https://beian.miit.gov.cn/" target="_blank" class="legal-link icp">
            皖ICP备2024067408号-2
          </a>
        </div>
        
        <!-- <div class="footer-beian">
          <a href="http://www.beian.gov.cn/" target="_blank" class="beian-link">
            
            皖公网安备 34020302000466号
          </a>
        </div> -->
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background: var(--text-primary);
  color: rgba(255, 255, 255, 0.7);
  padding: var(--space-3xl) 0 var(--space-xl);
}

.footer-content {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: var(--space-3xl);
  padding-bottom: var(--space-2xl);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-brand {
  max-width: 300px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  margin-bottom: var(--space-md);
}

.footer-logo-img {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-md);
}

.footer-logo-text {
  font-size: 1.25rem;
  font-weight: 700;
  color: white;
}

.footer-tagline {
  font-size: 0.9375rem;
  line-height: 1.6;
}

.footer-links {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--space-xl);
}

.footer-column-title {
  font-size: 0.875rem;
  font-weight: 600;
  color: white;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--space-lg);
}

.footer-list {
  display: flex;
  flex-direction: column;
  gap: var(--space-sm);
}

.footer-list a {
  font-size: 0.9375rem;
  color: rgba(255, 255, 255, 0.6);
  transition: color var(--transition-fast);
}

.footer-list a:hover {
  color: white;
}

.footer-bottom {
  padding-top: var(--space-xl);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--space-md);
  text-align: center;
}

.footer-copyright p {
  font-size: 0.875rem;
}

.footer-legal {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  flex-wrap: wrap;
  justify-content: center;
}

.legal-link {
  font-size: 0.8125rem;
  color: rgba(255, 255, 255, 0.5);
  transition: color var(--transition-fast);
}

.legal-link:hover {
  color: white;
}

.legal-divider {
  color: rgba(255, 255, 255, 0.3);
}

.icp {
  color: rgba(255, 255, 255, 0.6);
}

.footer-beian {
  margin-top: var(--space-sm);
}

.beian-link {
  display: flex;
  align-items: center;
  gap: var(--space-xs);
  font-size: 0.8125rem;
  color: rgba(255, 255, 255, 0.5);
  transition: color var(--transition-fast);
}

.beian-link:hover {
  color: white;
}

.beian-icon {
  width: 16px;
  height: 16px;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: var(--space-2xl);
  }
  
  .footer-links {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .footer-brand {
    text-align: center;
    max-width: none;
  }
  
  .footer-logo {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .footer-links {
    grid-template-columns: 1fr;
    text-align: center;
  }
}
</style>
