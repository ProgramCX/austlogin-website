<template>
  <header class="header" :class="{ 'header-scrolled': isScrolled }">
    <div class="container header-content">
      <a href="#" class="logo">
        <img src="/logo.png" alt="Logo" class="logo-img" />
        <span class="logo-text">快接安理大校园网</span>
      </a>
      
      <nav class="nav" :class="{ 'nav-open': isMenuOpen }">
        <a href="#features" class="nav-link" @click="closeMenu">功能特性</a>
        <a href="#screenshots" class="nav-link" @click="closeMenu">应用截图</a>
        <a href="#download" class="nav-link" @click="closeMenu">下载安装</a>
        <a href="#tech" class="nav-link" @click="closeMenu">技术栈</a>
        <a 
          href="https://github.com/ProgramCX/AUSTLogin" 
          target="_blank" 
          class="nav-link nav-link-github"
          @click="closeMenu"
        >
          <svg class="icon" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
          </svg>
          GitHub
        </a>
      </nav>
      
      <button class="menu-toggle" @click="toggleMenu" :aria-expanded="isMenuOpen">
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: var(--space-md) 0;
  transition: all var(--transition-normal);
  background: transparent;
}

.header-scrolled {
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(20px);
  box-shadow: var(--shadow-sm);
  padding: var(--space-sm) 0;
}

.header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  display: flex;
  align-items: center;
  gap: var(--space-sm);
  font-weight: 700;
  font-size: 1.25rem;
  color: var(--text-primary);
}

.logo-img {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-md);
}

.logo-text {
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav {
  display: flex;
  align-items: center;
  gap: var(--space-xl);
}

.nav-link {
  font-size: 0.9375rem;
  font-weight: 500;
  color: var(--text-secondary);
  transition: color var(--transition-fast);
  display: flex;
  align-items: center;
  gap: var(--space-xs);
}

.nav-link:hover {
  color: var(--primary-color);
}

.nav-link-github {
  padding: var(--space-sm) var(--space-md);
  background: var(--bg-tertiary);
  border-radius: var(--radius-lg);
}

.nav-link-github:hover {
  background: var(--primary-color);
  color: white;
}

.icon {
  width: 18px;
  height: 18px;
}

.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  padding: var(--space-sm);
}

.menu-bar {
  width: 24px;
  height: 2px;
  background: var(--text-primary);
  border-radius: 2px;
  transition: all var(--transition-fast);
}

@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }
  
  .nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    flex-direction: column;
    justify-content: center;
    gap: var(--space-xl);
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(20px);
    opacity: 0;
    visibility: hidden;
    transition: all var(--transition-normal);
  }
  
  .nav-open {
    opacity: 1;
    visibility: visible;
  }
  
  .nav-link {
    font-size: 1.25rem;
  }
}
</style>
