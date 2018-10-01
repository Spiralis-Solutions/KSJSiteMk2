<template>
  <div class="main">
    <div class="navbar">
      <div v-bind:class="nvLogic" v-on:click="navToggle"></div>
      <div v-bind:class="navpaneLogic">
        <button class="home" v-on:click="navToggle(); $router.push('/')">Home</button>
        <button class="contact" v-on:click="navToggle(); $router.push('/Contact')">Contact</button>
        <button class="Portfolio" v-on:click="navToggle(); $router.push('/Portfolio')">Portfolio</button>
          <a href="https://twitter.com/KrisStJohn27" class="twitter">Twitter</a>
          <a href="https://www.linkedin.com/in/kristoffer-st-john-948944145/" class="linkedin">LinkedIn</a>
          <a href="https://github.com/Spiralis-Solutions" class="github">Github</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  created () {
    let vue = this
    function toggleShow () {
      if (vue.show === 0) {
        vue.show = 1
      } else if (vue.show === 1) {
        vue.show = 2
      } else if (vue.show === 2) {
        vue.show = 3
      } else if (vue.show === 3) {
        vue.show = 4
      } else if (vue.show === 4) {
        vue.show = 5
      } else if (vue.show === 5) {
        vue.show = 0
      }
    }
    setInterval(toggleShow, 4000)
  },
  computed: {
    nvLogic: function () {
      return {
        nv: true,
        navButtonAnimation: this.isToggled,
        navButtonAnimationExit: !this.isToggled && !this.first
      }
    },
    navpaneLogic: function () {
      return {
        navpane: this.first,
        navpaneAnimation: this.isToggled,
        navpaneAnimationExit: !this.isToggled && !this.first
      }
    }
  },
  data () {
    return {
      toggled: false,
      isToggled: false,
      first: true
    }
  },
  methods: {
    navToggle: function () {
      // Nav button functionality
      if (window.innerWidth < 700) {
        if (this.toggled === false) {
          this.toggled = true
          this.isToggled = true
          this.first = false
        } else if (this.toggled === true) {
          this.toggled = false
          this.isToggled = false
        }
      } else {
        this.$router.push('/')
      }
    }
  }
}
</script>

<style scoped lang='less'>

  .main {
    margin-top: none;
    position: absolute;
    width: 50%;
    height: 100px;
    z-index: 2;
  }

  .navpane {
    display: none;
    position: absolute;
    margin-top: none;
  }

  .navbar {
    margin-top: none;
  }

  .nv {
    right: 0;
    position: fixed;
    margin-right: 2vw;
    top: 2vh;
    width: 80px;
    height: 80px;
    overflow: hidden;
    z-index: 10;
    background-repeat: no-repeat;
    background-image: url("../assets/navbuttonAnimationWhite.svg");
    transform: scale(.70);
  }

  @keyframes navButtonAnimation {
    100% {background-position: -1440px;}
  }

  @keyframes navButtonAnimationReverse {
    0% {background-position: -1440px;}
    100% {background-position: 0px;}
  }

  @keyframes navpaneAnimation {
    0% { right: -220px; }
    50% { right: 0px;}
    100% { right: -0px;}
  }

  @keyframes navpaneAnimationReverse {
    0% { right: -0px;}
    50% { right: 0px;}
    100% { right: -420px; }
  }

  .navButtonAnimation {
    animation: navButtonAnimation .3s steps(9);
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  .navButtonAnimationExit {
    animation: navButtonAnimationReverse .2s steps(6);
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  .navpaneAnimation {
    position: fixed;
    animation: navpaneAnimation .3s steps(9);
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
    z-index: 9;
    width: 100%;
    height: 100%;
    background:rgba(0,0,0,0.8);
    display: grid;
    grid-template-rows: repeat(12,1fr);
  }

  .navpaneAnimationExit {
    position: fixed;
    animation: navpaneAnimationReverse .3s steps(6);
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
    z-index: 9;
    width: 100%;
    height: 100%;
    background:rgba(0,0,0,0.8);
    display: grid;
    grid-template-rows: repeat(12,1fr);
  }

  button {
    letter-spacing: 1.3px;
    -webkit-animation-duration: .25s;
    animation-duration: .25s;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    -webkit-animation-timing-function: ease-in-out;
    animation-timing-function: ease-in-out;
    animation-iteration-count: 1;
    -webkit-animation-iteration-count: 1;
    background: none;
    border: none;

  }

  button:hover {
    animation-name: bounce;
    -moz-animation-name: bounce;
  }

  .home {
    font-size: 2em;
    font-weight: 300;
    text-align: right;
    grid-row: 3;
    margin-right: 3vw;
    color: #e0d186;
  }
  .Portfolio {
    font-size: 2em;
    font-weight: 300;
    text-align: right;
    grid-row: 4;
    margin-right: 3vw;
    color: #e0d186;
  }

  .contact {
    font-size: 2em;
    font-weight: 300;
    text-align: right;
    grid-row: 5;
    margin-right: 3vw;
    color: #e0d186;
  }
  a {
    font-size: 1.5em;
    text-align: right;
    text-decoration: none;
    margin-right: 5vw;
    color: #e0d186;
    font-weight: 300;
  }
  .linkedin {
    grid-row: 9;
  }
  .twitter {
    grid-row: 10;
  }
  .github {
    grid-row: 11;
  }

  @media (min-width: 700px) {

    .nv {
      display: none;
    }

    .navpane {
      position: absolute;
      top: 0;
      width: 100vw;
      height: 15vh;
      z-index: 9;
      display: grid;
      font-weight: bold;
    }
    .linkedin,.twitter, .github {
      grid-column: 3;
      font-size: 2em;
    }
    .linkedin {
      grid-row: 3;
    }
    .twitter {
      grid-row: 4;
    }
    .github {
      grid-row: 5;
    }
    .home, .Portfolio, .contact {
      text-align: left;
      padding-left: 5vw;
      margin-right: 0;
    }
  }
</style>
