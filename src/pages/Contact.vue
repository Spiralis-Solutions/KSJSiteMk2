<template>
  <div class="main">
    <div class="flo" data-aos="fade-up"></div>
      <h1 data-aos="fade-up">Contact</h1>
      <p data-aos="fade-up">Krisstjohn96@gmail.com</p>
      <p data-aos="fade-up">(480)-770-4245</p>
      <p data-aos="fade-up">(Please Email to Schedule Calls First)</p>
  </div>
</template>

<script>
import AOS from 'aos'
export default {
  name: 'Contact',
  created () {
    AOS.init()
  }
}
</script>

<style scoped lang="less">
.main {
  overflow-y: scroll;
  width: 100vw;
  height: 100vh;
  position:absolute;
  display: grid;
  grid-template-columns:  5vw repeat(4, 1fr) 5vw;
  grid-template-rows: repeat(10, 1fr);
  background-color: #38332c;
}
/* width */
::-webkit-scrollbar {
    width: 3px;
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
p {
  color: #e0d186;
  font-size: 1.3em;
  font-weight: 300;
  text-align: center;
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
}
@media (min-width: 700px) {
  h1 {
    grid-column-start: 3;
    grid-column-end: 5;
  }
  p {
    font-size: 2em;
  }
}
</style>
