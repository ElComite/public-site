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

            <div class="details">

                <a href="https://www.kamstrup.com/es-es"><img src="/malaga/img/kamstrup.svg" alt="kamstrup"></a>
                <h4>Edificio La Rosa</h4>
                <p>Av. de Jorge Luis Borges, 14<br> 29010 Málaga</p>

                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3198.0948133999555!2d-4.465928584712342!3d36.720284079965!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xee76c570d9f4aad2!2sEdificio+La+Rosa!5e0!3m2!1ses!2ses!4v1538937301805" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

            </div>


          </section>
    </div>

    <footer>
        <div class="container">
            <div class="left">elComite 2018</div>
            <div class="right">
                <h4>Evento apoyado por</h4>
                <a href="https://www.kamstrup.com/es-es"><img src="/malaga/img/kamstrup.svg" alt="kamstrup"></a>
            </div>
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

  #place
    h4
      margin 0
      margin-bottom 10px
      font-size 20px
    img
        max-width 200px
        height: auto

    
</style>


