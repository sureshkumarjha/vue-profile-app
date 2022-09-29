<template>
  <div>
    <section>
      <div className="tc flex justify-center" id="section1">
        <div className='overlay theme-light-blue-bg'></div>
        <div className='flex flex-column justify-around items-center'>
          <div>
            <img :src="profile" height="250" className='ma1 br-100 shadow-1 avtar-shadow' />
            <div className='subheading'>HEY! I AM</div>
            <div className='f2 heading pa2 b animate__animated animate__bounceInDown'>Suresh Kumar Jha</div>
            <SlidingTextComponent />
          </div>
          <div class="arrow-container mt5">
            <div>
              <div class="arrow" @click="goToPage('about')"></div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="theme-light-blue-bg">
      <AboutComponent />
      <ProjectComponent />
    </div>
  </div>
</template>

<script>
import avtar from "../assets/avtar.jpg";
import profile from "../assets/suresh.jpg";
import SlidingTextComponent from "@/components/SlidingTextComponent.vue";
import AboutComponent from "@/components/AboutComponent.vue";
import ProjectComponent from "@/components/ProjectComponent.vue";

export default {
  name: "HomeView",
  data() {
    return {
      avtar: avtar,
      profile: profile,
    }
  },
  components: {
    SlidingTextComponent,
    AboutComponent,
    ProjectComponent
  },
  methods: {
    goToPage(e) {
      let ele = document.getElementById(e);
      if (ele !== null) {
        ele.scrollIntoView({
          block: 'start',
          behavior: 'smooth',
          inline: 'start'
        });
      }
      document.getElementById("mySidenav").style.height = "0";
    }
  }
};
</script>

<style>
.avtar-shadow {
  z-index: 1;
}

.arrow {
  box-sizing: border-box;
  height: 5vw;
  width: 5vw;
  border-style: solid;
  border-color: #3e64ff;
  border-width: 0px 2px 2px 0px;
  transform: rotate(45deg);
  transition: border-width 150ms ease-in-out;
}

.arrow:hover {
  border-bottom-width: 6px;
  border-right-width: 6px;
}

.arrow-container {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0e242d00;
}

@media only screen and (max-width: 700px) {
  .arrow {
    height: 10vw;
    width: 10vw;
    margin-bottom: 3em;
  }
}
</style>
