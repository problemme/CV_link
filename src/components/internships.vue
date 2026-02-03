<template>
  <section class="internships">
    <h2 class="title">Internships</h2>

    <div class="timeline">
      <div 
        class= "timeline-item"
        :class="{ left: index % 2 === 0, right: index % 2 === 1 }"
        v-for="(intern, index) in internships"
        :key="index"
        >
        <div class="card">
          <h3 class="company">{{ intern.company }}</h3>
          <div class="role">{{ intern.role }}</div>
          <ul class="details">
            <li v-for="(detail, i) in intern.details" :key="i">
                <span v-if="typeof detail === 'string'">{{ detail }}</span>
                <span v-else>
                  {{ detail.text }}
                  <a v-if="detail.link" :href="detail.link" target="_blank">{{ detail.linkText }}</a>
                </span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const internships = [
    {
        company: 'TikTok',
        role: 'Front-end Development Engineer Intern',
        details: [
            'Design front-end pages for Coze using JS frameworks',
            'Participate in research and implementation of LLM-based agent frameworks'
        ]
    },
    {
        company: 'XIAOMI',
        role: 'Simulation Test Development Engineer Intern',
        details: [
            'Develop navigation-related evaluators based on actual vehicle data from the back-end channel and build a decision-making system for analysis, achieving an accuracy rate of 80%',
            'Develop the simulation evaluator’s back-end interface (Python),define the interface Proto in support of completing the annotation and configuration at the front end',
            'Improve the visualization of self-driving information at the front-end webpage by adding the acceleration part'
    ]
    },
    {
        company: 'State Grid Subsidiary',
        role: 'AI Algorithm Intern',
        details: [
  {
    text: 'Based on Tesseract, optimize the model recognition performance for grayscale images by 12%'
  },
  {
    text: 'Design an invoice recognition web interface using Streamlit for users to return the identification text',
    link: 'https://github.com/problemme/-/blob/main/OCR_front_end',
    linkText: 'OCR_front_end'
  }
]

    },
    {
        company: 'HUACHUANG Securities',
        role:'Fixed Income Research Intern',
        details: [
            'Use SQL and EXCEL to collect and analyze the ifind bond index, and fit the sample bar interpolation function',
            'Use python decision tree to classify user behavior, maximize information gain, and analyze the relationship between insurance principal and insurance period'
        ]
    }
]
</script>

<style scoped>
.internships {
  max-width: 1000px;
  margin: 30px auto 40px;
}

.title {
  text-align: center;
  font-size: 28px;
  font-weight: 600;
  margin-bottom: 20px;
}

.timeline {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 40px;
  padding: 40px 0;
}

.timeline::before {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
  width: 2px;
  background-color: #e0e0e0;
  transform: translateX(-75%);
}

.timeline-item {
    display:flex;
    position: relative;
    width: 50%;
    padding: 10px 20px;
}
.details {
  list-style-position: inside;   
  padding-left: 20px;
  margin: 8px 0 0;
  text-align: left;
}

.details li {
  text-align: left;
  line-height: 1.6;
  margin-bottom: 6px;
}
.card {
  max-width: 700px;
  background: #fff;
  border-radius: 2px;
  padding: 16px;
  box-shadow: 0 6px 20px rgba(0,0,0,0.06);
}

</style>
