<template>
    <article class="agenda-item">
        <header class="time">
            <h5>{{item.time}}</h5>
            <h4 class="title">{{item.name}}</h4>
        </header>
        <section class="speaker_container" v-if="item.type=='talk'">
        
            <div class="avatar">
                <img :src="item.avatar" :alt="item.name">
            </div>
            <div class="talk" >
                <p v-html="nl(item.bio)"></p>
                <h5 v-if="item.talk.title">Su charla: {{item.talk.title}}</h5>
                <p>{{item.talk.description}}</p>
            </div>
        </section>

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