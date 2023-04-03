<template>
  <div>
    <navigation-bar />
    <heading />
    <features />
    <project />
    <footer-part />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      navOpacity: 0,
      hcOpacity: 1,
      projOpacity: 0
    }
  },
  methods: {
    handleScroll (event) {
      let scroll = window.scrollY;
      console.log(scroll);
      let bottomScroll = scroll+window.innerHeight;
      // navbar and header opacity =============================
      if(scroll > 100 && this.navOpacity < 1){
          this.navOpacity+=.1;
          this.hcOpacity-=.1;
      } else if (scroll < 100 && this.navOpacity > 0) {
          this.navOpacity-=.1;
          this.hcOpacity+=.1;
      }
      document.getElementById("hContainer").style.opacity = this.hcOpacity;
      document.getElementById("navigation").style.backgroundColor = "rgba(18,18,18,"+this.navOpacity+")";
      document.getElementById("navContainer").style.backgroundColor = "rgba(18,18,18,"+this.navOpacity+")";

      // features =============================
      if(scroll > (window.innerHeight/2)-100 && this.projOpacity < 1){
          this.projOpacity+=.1;
      } else if(scroll < (window.innerHeight/2)-100 && this.projOpacity > 0){
          this.projOpacity-=.1;
      }
      document.getElementById("skills").style.opacity = this.projOpacity;
      document.getElementById("projects").style.opacity = this.projOpacity;
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll);
  }

}
</script>
