<template>
    <article class="agenda-item">
        <header>
            <h5>Hora sin determinar</h5>
        </header>


        <div class="talk">
            <h4 class="title">{{speaker.talk.title}}</h4>
            <p class="talk">{{speaker.talk.description}}</p>
        </div>

        <h5>Ponente</h5>
        <footer>
                <div class="avatar">
                    <img :src="speaker.avatar" :alt="speaker.name">
                </div>
                <div class="desc">
                    <h4>{{speaker.name}}</h4>
                    <p><a :href="speaker.links.twitter">twitter</a></p>
                </div>
        </footer>



      




    </article>
</template>

<script>

import NavLink from '../theme/NavLink'

export default {
    components: {NavLink},
    props: ["speaker"],
    data () {
        return {
        }
    }
}
</script>

<style lang="stylus">
@import './styles/config.styl'
.agenda-item 
    margin 120px 0
    h4 
        font-size 22px
        margin-top 0
        margin-bottom 4px


    p
        margin 0 0 12px 0
    .talk 
        padding 0px 0 10px 0
        p 
            font-size 18px
            line-height 24px
        h4.title 
            font-size 40px
            margin-bottom 16px
            margin-top 14px
    footer
        display flex
        align-content flex-start
        flex-flow row wrap;
        margin-bottom 24px

        .avatar
            order 1
            width 15%
            img
                max-width 100%
                height auto
            .desc
            order 2
            max-width 85%
            padding-left 40px
        p
            font-size 13px

    h5 
        text-transform uppercase
        margin-bottom 12px
        margin-top 0
        font-size 16px

    header
        margin-bottom 12px
        padding-bottom: 8px
        border-bottom 1px solid #eee
        h5 
            margin 0
.agenda-item:first-child
    margin-top 64px
</style>