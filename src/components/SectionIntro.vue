<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">{{title}}</h1>
                    <h2 class="subtitle">
                        {{subtitle}}
                    </h2>
                </div>
            </div>
        </section>
    </div>
</template>
<script>
export default {
    props:['title','subtitle'],
    data () {
        return {}
    },
    computed: {},
    mounted () {},
    methods: {},
    components: {}
}
</script>
<style scoped>

</style>