<template>
  <div
    class="home"
  >
  

    <section id="header">

          <Hero :title="config.title" 
              :description="config.claim"
              :ctaText="config.ctaText"
              :date="config.date"></Hero>

    </section>


    <section id="description">
      <Content custom/>
    </section>


    <section id="agenda">
        <h2>Agenda</h2>

        <AgendaItem v-for="speaker in config.speakers" 
                    :speaker="speaker"></AgendaItem>
                    
    </section>

    <footer>
      elComité 2018
    </footer>



  </div>
</template>

<script>
import Vue from 'vue'
import nprogress from 'nprogress'
import Hero from './Hero'
import AgendaItem from './AgendaItem'

export default {
  components: { Hero, AgendaItem },

  data() {
    return {
      config: {}
    }
  },
  mounted(){
       const { frontmatter } = this.$page
       return this.config = frontmatter
  }
  
}
</script>


