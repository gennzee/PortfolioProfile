<template>
  <div>
    <Header/>
    <Content/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Content from '@/components/Content.vue'
import $ from 'jquery'
import '@/assets/js/all.min.js'
import 'bootstrap'
import '@/assets/js/jquery.easing.min.js'

export default {
  name: 'Home',
  components: {
    Header,
    Content
  },
  mounted(){
    // Smooth scrolling using jQuery easing
    $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (location.pathname.replace(/^\//, "") == this.pathname.replace(/^\//, "") && location.hostname == this.hostname) {
            var target = $(this.hash);
            target = target.length ? target : $("[name=" + this.hash.slice(1) + "]");
            if (target.length) {
                $("html, body").animate({scrollTop: target.offset().top}, 500, "easeInOutExpo");
                return false;
            }
        }
    });

    // Closes responsive menu when a scroll trigger link is clicked
    $(".js-scroll-trigger").click(function () {
        $(".navbar-collapse").collapse("hide");
    });

    // Activate scrollspy to add active class to navbar items on scroll
    $("body").scrollspy({
        target: "#sideNav"
    });
  }
}
</script>

<style scoped>
@import url("~@/assets/css/styles.css");
@import url("https://fonts.googleapis.com/css?family=Saira+Extra+Condensed:500,700");
@import url("https://fonts.googleapis.com/css?family=Muli:400,400i,800,800i");
</style>