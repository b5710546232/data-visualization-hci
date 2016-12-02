<template>
    <div class="root">
        <a href="#" @click="scollTo('#my-navbar')" >
            <span>
                                <span class="columns">
                                    <i class="fa fa-arrow-up fa-4x"></i>
                                </span>
            <span class="columns is-centered">
                                    Go to top
                                </span>
            </span>
        </a>
    </div>
</template>
<script>
import scrollToElement from 'scroll-to-element'
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {},
    methods: {
                 scollTo(e){
      event.preventDefault()
      scrollToElement(e, {
        offset: 0,
        ease: 'outBack',
        duration: 500
      })
    }
    },
    components: {}
}
</script>
<style scoped>

</style>