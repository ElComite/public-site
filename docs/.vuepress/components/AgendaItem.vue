<template>
    <article>

      <h4>{{speaker.name}}</h4>
      <p>
        <img :src="speaker.avatar" :alt="speaker.name">
      </p>

      <h5>Su charla</h5>
      <h4>{{speaker.talk.title}}</h4>
      <p>{{speaker.talk.description}}</p>



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