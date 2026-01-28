<template>
  <section class="research">
    <h2 class="title">Research % Projects</h2>

    <div class="research-grid">
      <div
        class="research-card"
        v-for="(item, index) in research"
        :key="index"
      >
        <h3 class="research-title">{{item.title}}</h3>
        <div class="research-affiliation">{{ item.affiliation }}</div>
        <p class="research-desc">{{item.desc}}</p>

        <ul class="research-details">
          <li v-for="(d, i) in item.details" :key="i">
            {{d}}
          </li>
        </ul>

        <a
          v-if="item.link"
          :href="item.link"
          target="_blank"
          class="research-link"
        >
          {{ item.linkText }}
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>

  const research = [
  {
    title: 'Automatic Composition Based on Mamba',
    affiliation: 'Jilin University · Research Assistant',
    desc: 'Music generation and quality prediction using sequence models.',
    details: [
      'Preprocessed symbolic music into time-series representations',
      'Systematically optimize key hyperparameters including learning rate, number of layers, and neurons',
      'Evaluated generation quality of Bach-style compositions'
    ]
  },
  {
    title: 'Kalman Filter & SSM for Human Pose Prediction',
    affiliation: 'Jilin University · Graduation Thesis',
    desc: 'Sensor fusion and state-space modeling for motion prediction.',
    details: [
      'Rebuilt EgoLocate 3D human pose system',
      'Conducte comparative experiments on visual-inertial inputs',
      'Replaced RNN layers with Mamba, achieving ~10% improvement'
    ]
  },
  {
    title: 'Linear Regression of PM10 & PM2.5',
    affiliation: 'NUS Summer School',
    desc: 'Statistical analysis of particulate matter concentrations.',
    details: [
      'Analyzed distribution similarity using Q-Q plots',
      'Built regression model with R² = 0.7381'
    ]
  },
  {
    title: 'Cross-lingual Fanfiction Data Platform',
    affiliation: 'Independent Project',
    desc: 'A system for large-scale text collection and translation.',
    details: [
      'Designed a crawler-based pipeline for text archiving',
      'Integrated machine translation to improve accessibility',
      'Built a web interface for search and reading'
    ],
    link: 'https://github.com/problemme/Whatsyourfavorite',
    linkText: 'Whatsyourfavorite'
  }
]
</script>

<style scoped>
.research-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  margin-top: 32px;
}

.research-card {
  background: #fff;
  border-radius: 14px;
  padding: 20px;
  box-shadow: 0 8px 24px rgba(0,0,0,0.06);
}

.research-title {
  font-size: 1.05rem;
  font-weight: 600;
}

.research-affiliation {
  font-size: 0.85rem;
  color: #666;
  margin-bottom: 8px;
}

.research-desc {
  font-size: 0.9rem;
  margin-bottom: 10px;
}

.research-details {
  max-width: 520px;
  margin: 12px auto 0;
  padding-left: 0;
  /*圆点变成正文一部分*/
  list-style-position: inside;
  font-size: 0.88rem;
  line-height: 1.6;
}

.research-details li {
/*控制文字起始位置*/
  padding-left: 50px;
  text-align: left;
  line-height: 1.6;
  font-size: 0.9rem;
}

.research-link {
  display: inline-block;
  margin-top: 10px;
  color: #1a73e8;
  text-decoration: none;
}
</style>