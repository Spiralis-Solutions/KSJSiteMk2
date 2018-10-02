<template>
  <div class="main">
    <div class="title" data-aos="flip-left">
    <h1>Kristoffer St John</h1>
    <h2>UX Developer</h2>
  </div>
  <div class="flo" data-aos="fade-up"></div>
  <div class="stuff">
    <h3 data-aos="fade-up">Web & App Development</h3>
    <p data-aos="fade-up">Ultra-responsive and lightweight hybrid web app development. Creating SPAs with the most cutting edge web development technologies available.</p>
    <h3 data-aos="fade-up">Creative UI Design</h3>
    <p data-aos="fade-up">Enterprise quality design and architecture, detail focused and User Oriented development, while providing gorgeous presentation and polish.</p>
    <h3 data-aos="fade-up">Innovative Technologies</h3>
    <p data-aos="fade-up">Using VueJS and the QWC-VENUMM full stack, I can deploy lightning fast applications to any platform with ease.</p>
  </div>
  <div class="skills">
    <h4 data-aos="fade-up">Skills and Knowledge</h4>
    <p class="list" data-aos="fade-up">HTML5, CSS3, Javascript, VueJS and associated APIs, Express, NodeJS, Ubuntu Servers, Cordova, Quasar, Webpack, MongoDB, Mongoose, Amazon Web Services, JIRA, Git Workflow</p>
    <p class="list" data-aos="fade-up">Agile, Scrum, JIRA, Kanban, QWC-VENUMM, Adobe Photoshop, Illustrator, Premiere</p>
    <h4 data-aos="fade-up">Project Experience</h4>
    <ul data-aos="fade-up">
    <li>Building and deploying full SPAs to all platforms.</li>
    <li>Creating business software solutions such as CRMs, Custom Management and Warehouse scheduling software</li>
    <li>Created applications with geolocation, Stripe payment, Invoicing, CSV, Task Automation,
scheduling, file uploading, and some Machine Learning.
</li>
<li>-UX/UI focused design and code, from simple front end websites to complicated architectures.</li>
  </ul>
  <h4 data-aos="fade-up">Education</h4>
  <p class="list" data-aos="fade-up">Full Stack Web Development Certification; Woz-U Coding Bootcamp</p>
  <p class="list" data-aos="fade-up">Personal and professional references available on request.</p>
  </div>
  </div>
</template>

<script>
import AOS from 'aos'
export default {
  name: 'PageIndex',
  created () {
    AOS.init()
  }
}
</script>

<style scoped lang="less">
/* width */
::-webkit-scrollbar {
    width: 0px;
    height:3px;
}

/* Track */
::-webkit-scrollbar-track {
    box-shadow: inset 0 0 5px transparent;
    border-radius: 15px;
    border: none;
}

/* Handle */
::-webkit-scrollbar-thumb {
    background: #666;
    border-radius: 15px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
    background: #555;
}
.main {
  overflow-y: scroll;
  z-index: 1;
  width: 100vw;
  height: 430vh;
  position:absolute;
  display: grid;
  grid-template-rows: repeat(43, 1fr);
  grid-template-columns: 5vw repeat(4, 1fr) 5vw;
  background-color: #38332c;
}
h1 {
  text-align: center;
  font-size: 2em;
  font-weight: lighter;
  letter-spacing: 1px;
  font-family: 'Judson', serif;
}
h2 {
    font-size: 1.5em;
    text-align: center;
    letter-spacing: 1px;
    font-family: 'Judson', serif;
}
.stuff {
  background-color: #e0d186;
  grid-row-start: 11;
  grid-row-end: 21;
  grid-column-start: 1;
  grid-column-end: 7;
}
h3 {
  font-size: 1.8em;
  font-weight: 300;
  text-align: center;
  font-family: 'Judson', serif;
  color: #38332c;
}
p {
  text-align: center;
  padding: 2vw;
  font-size: 1.2em;
  font-weight: 300;
  color: #38332c;
}
.title {
  grid-column-start: 2;
  grid-column-end: 6;
  color: #e0d186;
  grid-row-start: 5;
  grid-row-end: 7;
  border: 2px solid #e0d186;
  outline: 2px solid #e0d186;
  outline-offset: -3vw;
}
.flo {
  background-image: url('../assets/flourish2.svg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  grid-column-start: 2;
  grid-column-end: 6;
  grid-row: 7;
}
.skills {
  grid-row-start: 22;
  grid-row-end: 30;
  grid-column-start: 1;
  grid-column-end: 7;
}
h4 {
  text-align: center;
  color: #e0d186;
  font-size: 2em;
  font-family: 'Judson', serif;
}
.list {
  color: #e0d186;
  font-size: 1.3em;
  text-align: center;
  padding: 2vw;
}
li {
  color: #e0d186;
  font-size: 1.3em;
  font-weight: 300;
  padding: 2vw;
}
@media (min-width: 700px) {
  .title {
    outline-offset: -1vw;
    grid-column-start: 3;
    grid-column-end: 5;
    grid-row-start: 5;
    grid-row-end: 7;
  }
  h1 {
    font-size: 2.3em;
  }
  h2 {
    font-size: 1.8em;
  }
  h3 {
    font-size: 2em;
  }
  p, .list, li {
    width: 60vw;
    margin-left: 20vw;
    font-size: 1.5em;
  }
  .flo {
    grid-column-start: 1;
    grid-column-end: 7;
    height: 15vh;
    grid-row: 7;
  }
}
@media (min-width: 1000px) {
  .title {
    outline-offset: -1vw;
    grid-column-start: 3;
    grid-column-end: 5;
    grid-row-start: 5;
    grid-row-end: 8;
  }
  .stuff {
    grid-row-start: 11;
    grid-row-end: 22;
  }
}
</style>
