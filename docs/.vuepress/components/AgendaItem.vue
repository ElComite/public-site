<template>
    <article class="agenda-item">
        <header class="time">
            <h5>{{item.time}}</h5>
        </header>


        <div class="talk" v-if="item.type=='talk'">
            <h4 class="title">{{item.talk.title}}</h4>
            <p class="talk" v-html="nl(item.talk.description)"></p>
        </div>

        <div class="talk" v-if="item.type=='slot'">
            <h4 class="title">{{item.name}}</h4>
        </div>

        
        <footer class="speaker-cont" v-if="item.type=='talk'">
                <h5>Ponente</h5>
                <div class="speaker">
                    <img class="avatar" :src="item.avatar" :alt="item.name">
                    
                    <div class="desc">
                        <h4>{{item.name}} <a :href="item.links.twitter"><img src="/img/twitter.svg" alt=""></a></h4>
                        <p></p>
                    </div>
                </div>
        </footer>

    </article>
</template>

<script>

import NavLink from '../theme/NavLink'

export default {
    components: {NavLink},
    props: ["item"],
    data () {
        return {
        }
    },
    methods: {
        nl(str) {
            if (typeof str === 'undefined' || str === null) {
                return '';
            }
            var breakTag = '<br>';
            return (str + '').replace(/([^>\r\n]?)(\r\n|\n\r|\r|\n)/g, '$1' + breakTag + '$2');

        }
    }
}
</script>