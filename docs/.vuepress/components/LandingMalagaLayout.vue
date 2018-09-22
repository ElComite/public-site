<template>




  <div>
  
    <section id="header">

          <Hero :title="config.title" 
              :description="config.claim"
              :ctaText="config.ctaText"
              :bgImage="config.bgimage"
              :date="config.date"></Hero>

    </section>



    <div class="container">
          <section id="description">
            <Content custom/>
          </section>


          <section id="agenda">
              <h2 class="section-title">Agenda</h2>

              <AgendaItem v-for="agendaItem in config.agenda" 
                          :key="agendaItem.name"
                          :item="agendaItem"></AgendaItem>

          </section>


          <section id="place">
            <h2 class="section-title">Localización</h2>
            <p>Pronto más información</p>
          </section>
    </div>

    <footer>
        <div class="container">
          elComité 2018
        </div>
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

<style lang="stylus">

@require './styles/elements'


  #description 
    text-align center
    font-size 1.6rem
    line-height 1.8rem
    margin-top 3rem
    margin-bottom 6rem
    color #666


    
</style>


