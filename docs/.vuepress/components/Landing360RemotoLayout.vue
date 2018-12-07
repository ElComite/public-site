<template>




  <div id="landing_remoto">
  
    <header id="top">

      <div class="container">
        <a href="/" class="logo"></a>

        <div class="title">

            <h2>22 de Diciembre <strong>Bilbao</strong></h2>
            <h1>[trabajar en remoto]</h1>
        </div>
      </div>

          

    </header>



    <div class="container">
          <section id="description">
            <h4 class="hashtag">#360remoto</h4>
            <Content custom/>
            <a href="" class="cta button">Entradas aún no disponibles</a>
          </section>


          <section id="agenda">
              <h2 class="section-title">Agenda</h2>

              <SpeakerItem v-for="agendaItem in config.agenda" 
                          :key="agendaItem.name"
                          :item="agendaItem"></SpeakerItem>

          </section>


          <section id="place">
            <h2 class="section-title">Localización</h2>

            <div class="details">

                <h4>Auzo Factory Irazabal Matiko</h4>
                <p>Matiko Kalea, 6, 48007<br> Bilbo, Bizkaia</p>

                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2905.220718133235!2d-2.926488384395989!3d43.26775158528699!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd4e4fc476ca645d%3A0x8527a25d79badd9!2sAuzo+Factory+Irazabal+Matiko!5e0!3m2!1ses!2ses!4v1544116627802" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
            </div>


          </section>
    </div>

    <footer>
        <div class="container">
            <div class="left">elComite 2018</div>
            <div class="right">
                <h4>Evento apoyado por</h4>
                <a href="http://www.bilbao.eus/BilbaoEkintza/es/index.html"><img src="/remoto/img/logo_bilbao_ekintza.png" alt="Bilbao Ekintza"></a>
            </div>
        </div>
    </footer>


  </div>
</template>

<script>
import Vue from 'vue'
import nprogress from 'nprogress'
import Hero from './Hero'
import SpeakerItem from './SpeakerItem'

export default {
  components: { Hero, SpeakerItem },

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

@require './styles/remoto'


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


