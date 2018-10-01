<template>
  <div class="main">
    <div class="flo" data-aos="fade-up"></div>
    <h1 data-aos="fade-up">Portfolio</h1>
    <div class="n1" data-aos="fade-up"></div>
    <div class="n2" data-aos="fade-up"></div>
    <div class="n3" data-aos="fade-up"></div>
    <div class="m1" data-aos="fade-up"></div>
    <div class="m2" data-aos="fade-up"></div>
    <div class="m3" data-aos="fade-up"></div>
    <div class="t1" data-aos="fade-up"></div>
    <div class="q1" data-aos="fade-up"></div>
    <div class="k1" data-aos="fade-up"></div>
    <div class="k2" data-aos="fade-up"></div>
    <div class="links" data-aos="fade-up">
    <a href="https://neuronautsolutions.com/">Neuronaut Solutions</a><br/>
    <a href="https://www.mystic-crm.com/">Mystic CRM</a><br/>
    <a href="https://thumbnailconsulting.com/">Thumbnail Consulting</a><br/>
    <a href="https://quickvenom.org/">Quick Venom</a><br/>
    <a href="https://blakelateshow.com/">Blake Late Show</a>
  </div>
  </div>
</template>

<script>
export default {
  name: 'Portfolio'
}
</script>

<style scoped lang="less">
.main {
  overflow-y: scroll;
  width: 100vw;
  height: 230vh;
  position:absolute;
  display: grid;
  grid-template-columns:  5vw repeat(4, 1fr) 5vw;
  grid-template-rows: repeat(23, 1fr);
  grid-row-gap: 1vh;
  background-color: #38332c;
}
h1 {
  text-align: center;
  color: #e0d186;
  letter-spacing: 1px;
  font-size: 2.5em;
  font-family: 'Judson', serif;
  color: #e0d186;
  border: 2px solid #e0d186;
  grid-column-start: 2;
  grid-column-end: 6;
}
.flo {
  background-image: url('../assets/flourish2.svg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  grid-column-start: 2;
  grid-column-end: 6;
  height: 10vh;
}
.n1{
  background-image: url('../assets/n1.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 25vh;
  grid-column-start: 2;
  grid-column-end: 6;
}
.n2 {
  background-image: url('../assets/n2.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 2;
  grid-column-end: 4;
}
.n3{
  background-image: url('../assets/n3.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 4;
  grid-column-end: 6;
}
.m1{
  background-image: url('../assets/m1.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 2;
  grid-column-end: 4;
}
.m2{
  background-image: url('../assets/m2.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 4;
  grid-column-end: 6;
}
.m3{
  background-image: url('../assets/m3.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 2;
  grid-column-end: 4;
}
.t1{
  background-image: url('../assets/t1.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 4;
  grid-column-end: 6;
}
.q1{
  background-image: url('../assets/q1.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 2;
  grid-column-end: 4;
}
.k1 {
  background-image: url('../assets/k1.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 30vh;
  grid-column-start: 4;
  grid-column-end: 6;
}
.k2 {
  background-image: url('../assets/k2.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 100%;
  height: 25vh;
  grid-column-start: 2;
  grid-column-end: 6;
}
.links {
  text-align: center;
  color: #e0d186;
  font-size: 1.5em;
  grid-column-start: 2;
  grid-column-end: 6;
}
a {
  color: #e0d186;
  font-weight: 300;
  font-size: 1em;
}
@media (min-width: 700px) {
  .main {
    overflow-y: scroll;
    width: 100vw;
    height: 320vh;
    position:absolute;
    display: grid;
    grid-template-columns:  5vw repeat(4, 1fr) 5vw;
    grid-template-rows: repeat(32, 1fr);
    grid-row-gap: 1vh;
    background-color: #38332c;
  }
  h1 {
    grid-column-start: 3;
    grid-column-end: 5;
  }
  .n1{
    background-image: url('../assets/n1.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 50vh;
    grid-column-start: 2;
    grid-column-end: 6;
  }
  .n2 {
    background-image: url('../assets/n2.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 1;
    grid-column-end: 3;
  }
  .n3{
    background-image: url('../assets/n3.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 3;
    grid-column-end: 5;
  }
  .m1{
    background-image: url('../assets/m1.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 5;
    grid-column-end: 7;
  }
  .m2{
    background-image: url('../assets/m2.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 2;
    grid-column-end: 4;
  }
  .m3{
    background-image: url('../assets/m3.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 4;
    grid-column-end: 6;
  }
  .t1{
    background-image: url('../assets/t1.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 1;
    grid-column-end: 3;
  }
  .q1{
    background-image: url('../assets/q1.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 3;
    grid-column-end: 5;
  }
  .k1 {
    background-image: url('../assets/k1.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 40vh;
    grid-column-start: 5;
    grid-column-end: 7;
  }
  .k2 {
    background-image: url('../assets/k2.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    width: 100%;
    height: 50vh;
    grid-column-start: 1;
    grid-column-end: 7;
  }
}
</style>
