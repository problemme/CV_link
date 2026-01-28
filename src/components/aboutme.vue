<template>
  <section id = "aboutme" class="aboutme">
    <h2 class="title">About Me</h2>
    <div class="about-layout">
      <p>
        I am a senior undergraduate majoring in Computational Mathematics at Jilin University,
        with strong interests in Computer Science, Data Science, and AI.
        My experience spans front-end development, simulation systems for autonomous driving,
        and machine learning research, where I have worked with Python, C++, Vue and deep learning
        models such as Transformer and Mamba.
        I am applying for a CS / DS / AI Master program to further strengthen my theoretical
        foundation and build intelligent systems to address real-world problems.
      </p>
    </div>
    <!-- 技能与联系方式 -->
    <section class="info-bottom">
    <div class="info-block">
    <h3>Skills</h3>
    <p><strong>Programming:</strong> Python · C++ · SQL · JavaScript</p>
    <p><strong>Tools:</strong> Git · Linux · Docker</p>
    <p><strong>Research:</strong> Numerical Methods · Simulation · Optimization</p>
  </div>

  <div class="info-block">
    <h3>Contact</h3>
    <p><strong>Email:</strong>
      <a href="mailto:xinyuexia123@gmail.com">xinyuexia123@gmail.com</a>
    </p>
    <p><strong>GitHub:</strong>
      <a href="https://github.com/problemme" target="_blank">github.com/problemme</a>
    </p>
  </div>
</section>
  </section>
</template>

<style scoped>
.aboutme {
  max-width: 960px;
  margin: 0 auto;
  padding: 80px 24px;
}
.title {
/*只对正文居中*/
  text-align: center;
  margin-bottom: 32px;
}
.about-layout {
  text-align: left;
  line-height: 1.85;
  font-size: 1rem;
  color: #2c3e50;
}
.info-bottom {
  max-width: 720px;
  margin: 0 auto;
  padding: 48px 24px 80px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
}

.info-block h3 {
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 16px;
}

.info-block p {
  text-align: left;
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin: 8px 0;
}

.info-block strong {
  width: 110px;
  font-weight: 600;
  flex-shrink: 0;
}
</style>