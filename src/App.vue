<template>
    <div ref="lightgallery" id="lightgallery">
        <a v-for="(item, index) in items" :href="item.src">
            <img class="preview-img-item" :src="item.src">
        </a>
    </div>
</template>

<style scoped>
.preview-img-list {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
}
.preview-img-item {
    margin: 5px;
    max-width: 100px;
    max-height: 100px;
}
</style>

<script>
    import 'lightgallery.js/dist/css/lightgallery.css'
    import Lightgallery from 'lightgallery.js/dist/js/lightgallery'
    // import 'lg-thumbnail.js/dist/lg-thumbnail'

    console.log('start lightgallery')

    export default {
        data () {
            return {
                items: [{
                    src: '../img/Chrysanthemum.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Desert.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Hydrangeas.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Jellyfish.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Koala.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Lighthouse.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Penguins.jpg',
                    w: 1024,
                    h: 768
                }, {
                    src: '../img/Tulips.jpg',
                    w: 1024,
                    h: 768
                }]
            }
        },
        mounted () {
            const el = document.getElementById('lightgallery')
            // const el = this.$refs.lightgallery
            // const el = this.$el
            console.log('init lightgallery')
            Lightgallery(el)
        }
    }

</script>