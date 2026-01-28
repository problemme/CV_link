<script setup>
import { ref } from 'vue'
import aboutme from './components/aboutme.vue'
import internships from './components/internships.vue'
import research from './components/research.vue'
const current = ref('aboutme') // 默认显示 About Me
</script>

<template>
  <div class = "navigation">
<!--左侧导航，nav代表普通block放在最上方，因此需要共同的容器navigation-->
    <nav class ="nav-left">
      <a @click="current = 'aboutme'">About Me</a>
      <a @click="current = 'internships'">Internships</a>
      <a @click="current = 'research'">Research & Projects</a>
    </nav>
<!--右侧导航-->
    <main class="nav-right">
      <aboutme v-if="current === 'aboutme'" />
      <internships v-if="current === 'internships'" />
      <research v-if="current === 'research'" />
    </main>
  </div>
</template>

<style scoped>
.navigation {
  display: flex;
}
/*需要确保a为块级元素，即能够分行*/
.nav-left {
  width: 200px;
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;

  padding: 24px;
  background-color: #f7f7f7;
  border-right: 1px solid #ddd;

  display: flex;
  flex-direction: column;
  gap: 20px;
}

.nav-left a {
  display: block;         /* 保底：就算不用 flex 也能换行 */
  font-size: 16px;
  color: #333;
  text-decoration: none;
}

.nav-left a:hover {
  color: #646cff;
}

.nav-right {
  margin-left: 200px;
  padding: 40px;
}
</style>
