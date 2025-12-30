<template>
  <section id="features" class="section">
    <div class="container">
      <h2 class="section-title">功能特性</h2>
      <p class="section-subtitle">
        精心设计的功能，让校园网连接更智能、更便捷
      </p>
      
      <div class="features-grid">
        <div 
          v-for="(feature, index) in features" 
          :key="index"
          class="feature-card"
          :style="{ '--card-bg': feature.bgColor }"
        >
          <div class="feature-icon" :style="{ background: feature.iconBg }">
            <component :is="feature.icon" />
          </div>
          <h3 class="feature-title">{{ feature.title }}</h3>
          <p class="feature-description">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { h } from 'vue'

// 图标组件
const IconKey = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('path', { d: 'M21 2l-2 2m-7.61 7.61a5.5 5.5 0 1 1-7.778 7.778 5.5 5.5 0 0 1 7.777-7.777zm0 0L15.5 7.5m0 0l3 3L22 7l-3-3m-3.5 3.5L19 4' })
])

const IconRefresh = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('path', { d: 'M23 4v6h-6' }),
  h('path', { d: 'M1 20v-6h6' }),
  h('path', { d: 'M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15' })
])

const IconSignal = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('path', { d: 'M5 12.55a11 11 0 0 1 14.08 0' }),
  h('path', { d: 'M1.42 9a16 16 0 0 1 21.16 0' }),
  h('path', { d: 'M8.53 16.11a6 6 0 0 1 6.95 0' }),
  h('line', { x1: '12', y1: '20', x2: '12.01', y2: '20' })
])

const IconPalette = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('circle', { cx: '13.5', cy: '6.5', r: '.5' }),
  h('circle', { cx: '17.5', cy: '10.5', r: '.5' }),
  h('circle', { cx: '8.5', cy: '7.5', r: '.5' }),
  h('circle', { cx: '6.5', cy: '12.5', r: '.5' }),
  h('path', { d: 'M12 2C6.5 2 2 6.5 2 12s4.5 10 10 10c.926 0 1.648-.746 1.648-1.688 0-.437-.18-.835-.437-1.125-.29-.289-.438-.652-.438-1.125a1.64 1.64 0 0 1 1.668-1.668h1.996c3.051 0 5.555-2.503 5.555-5.555C21.965 6.012 17.461 2 12 2z' })
])

const IconMoon = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('path', { d: 'M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z' })
])

const IconLayout = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('rect', { x: '3', y: '3', width: '18', height: '18', rx: '2', ry: '2' }),
  h('line', { x1: '3', y1: '9', x2: '21', y2: '9' }),
  h('line', { x1: '9', y1: '21', x2: '9', y2: '9' })
])

const IconBell = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('path', { d: 'M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9' }),
  h('path', { d: 'M13.73 21a2 2 0 0 1-3.46 0' })
])

const IconList = () => h('svg', { viewBox: '0 0 24 24', fill: 'none', stroke: 'currentColor', 'stroke-width': '2' }, [
  h('line', { x1: '8', y1: '6', x2: '21', y2: '6' }),
  h('line', { x1: '8', y1: '12', x2: '21', y2: '12' }),
  h('line', { x1: '8', y1: '18', x2: '21', y2: '18' }),
  h('line', { x1: '3', y1: '6', x2: '3.01', y2: '6' }),
  h('line', { x1: '3', y1: '12', x2: '3.01', y2: '12' }),
  h('line', { x1: '3', y1: '18', x2: '3.01', y2: '18' })
])

const features = [
  {
    icon: IconKey,
    title: '一键登录',
    description: '快速登录校园网，告别繁琐的网页认证流程，一键完成网络连接。',
    bgColor: 'var(--card-blue)',
    iconBg: 'linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%)'
  },
  {
    icon: IconRefresh,
    title: '自动登录',
    description: '连接指定 WiFi 时自动完成认证，无需手动操作，真正的无感连接体验。',
    bgColor: 'var(--card-purple)',
    iconBg: 'linear-gradient(135deg, #8b5cf6 0%, #6d28d9 100%)'
  },
  {
    icon: IconSignal,
    title: '多通道支持',
    description: '支持校园网、中国移动、中国联通、中国电信等多种 ISP 通道选择。',
    bgColor: 'var(--card-green)',
    iconBg: 'linear-gradient(135deg, #10b981 0%, #059669 100%)'
  },
  {
    icon: IconPalette,
    title: 'Material You 设计',
    description: '采用 Material Design 3 设计语言，支持动态主题色，界面美观现代。',
    bgColor: 'var(--card-pink)',
    iconBg: 'linear-gradient(135deg, #ec4899 0%, #be185d 100%)'
  },
  {
    icon: IconMoon,
    title: '深色模式',
    description: '支持浅色/深色/跟随系统三种模式，保护眼睛，适应不同使用场景。',
    bgColor: 'var(--card-amber)',
    iconBg: 'linear-gradient(135deg, #f59e0b 0%, #d97706 100%)'
  },
  {
    icon: IconLayout,
    title: '自适应布局',
    description: '完美适配手机和平板设备，无论屏幕大小都能获得最佳体验。',
    bgColor: 'var(--card-cyan)',
    iconBg: 'linear-gradient(135deg, #06b6d4 0%, #0891b2 100%)'
  },
  {
    icon: IconBell,
    title: '登录通知',
    description: '自动登录时可选择显示通知提醒，让你随时了解网络连接状态。',
    bgColor: 'var(--card-blue)',
    iconBg: 'linear-gradient(135deg, #6366f1 0%, #4f46e5 100%)'
  },
  {
    icon: IconList,
    title: '登录日志',
    description: '记录每次登录的详细信息，方便排查问题，追踪连接历史。',
    bgColor: 'var(--card-green)',
    iconBg: 'linear-gradient(135deg, #22c55e 0%, #16a34a 100%)'
  }
]
</script>

<style scoped>
.features-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: var(--space-lg);
}

.feature-card {
  background: var(--card-bg);
  border-radius: var(--radius-xl);
  padding: var(--space-xl);
  transition: all var(--transition-normal);
  border: 1px solid transparent;
}

.feature-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
  border-color: var(--border-color);
}

.feature-icon {
  width: 56px;
  height: 56px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: var(--space-lg);
  color: white;
}

.feature-icon svg {
  width: 28px;
  height: 28px;
}

.feature-title {
  font-size: 1.125rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: var(--space-sm);
}

.feature-description {
  font-size: 0.9375rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

@media (max-width: 1024px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
}
</style>
