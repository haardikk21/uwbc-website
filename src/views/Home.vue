<template>
  <div class="home">
    <section class="section has-text-centered">
      <div class="container">
        <img src="../assets/logo.png" height="20%" width="20%"/>
        <section class="section"></section>
        <nav class="level">
          <div class="level-item has-text-centered">
            <div>
              <p class="heading is-size-5">Members</p>
              <animated-number class="title is-size-2" :value="members" :formatValue="formatPrice" :duration="1000" />
              <span class="title">+</span>
            </div>
          </div>
          <div class="level-item has-text-centered">
            <div>
              <p class="heading is-size-5">Events</p>
              <animated-number class="title is-size-2" :value="events" :formatValue="formatPrice" :duration="1000" />
              <span class="title">+</span>
            </div>
          </div>
        </nav>
      </div>
    </section>

    <section class="section has-background-white-ter">
      <div class="columns">
        <div class="column ">
          <div class="container is-fluid">
            <h1 class="title">Who are we?</h1>
            <p>
              UW Blockchain Club is a student-run organization at the University of Waterloo focusing on everything related to blockchain and cryptocurrencies.
              <br /> <br />
              We host events, workshops, meetups, and hackathons to introduce our members to the technology and promote blockchain adoption.
              <br /> <br /> 
              Our members consist of undergraduates, graduate students, and people from the Kitchener-Waterloo region. 
            </p>
          </div>
        </div>
        
        <div class="column has-text-centered is-two-thirds">
          <carousel :per-page="1" :autoplay="true" mouse-drag="false">
            <slide>
              <img src="../assets/img1.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img2.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img3.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img4.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img5.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img6.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img7.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img8.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img9.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img10.jpg" width=70% height=70%>
            </slide>
            <slide>
              <img src="../assets/img11.jpg" width=70% height=70%>
            </slide>
          </carousel>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import AnimatedNumber from "animated-number-vue";
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "home",
  components: {
    AnimatedNumber,
    Carousel,
    Slide
  },
  data() {
    return {
      members: 200,
      events: 5,
      tokens: 100
    };
  },
  methods: {
    formatPrice(value) {
      return `${value.toFixed(0)}`;
    }
  }
};
</script>