<template>
    <div class="container">
        <div class="box">
            <div class="is-flex carousel__item">
                <figure>
                    <img :src="currentItem.src"></img>
                    <figcaption class="has-text-centered">
                        <p class="title is-3">{{ currentItem.title }}</p>
                        <p class="subtitle is-5"> {{ currentItem.desc }} </p>
                        <span v-html="currentItem.other"></span>
                    </figcaption>
                </figure>
            </div>
            <nav class="pagination">
                <a class="button" @click="prevItem">Previous</a>
                <a class="button" @click="nextItem">Next</a>
                <ul>
                    <li v-for="(item, index) in carouselItems">
                        <a class="button" @click="showAtIndex(index)" :class="{ 'is-primary' : currentIndex == index }">{{ index+1 }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>
<script>
export default {
    name : 'vue-carousel',
    props: {
        carouselItems : {
            Type : Array,
            required : true
        }
    },
    created () {
        this.currentIndex = 0;
    },
    data () {
        return {
            currentIndex : 0,
        }
    },
    methods : {
        nextItem () {
            if(this.currentIndex == this.carouselItems.length-1){
                this.currentIndex = 0;
            }else{
                this.currentIndex++;  
            }
        },
        prevItem () {
            if(this.currentIndex == 0){
                this.currentIndex = this.carouselItems.length-1;
            }else{
                this.currentIndex--;  
            }
        },
        showAtIndex(index){
            this.currentIndex = index;
        }
    },
    computed: {
        currentItem(){
            return this.carouselItems[this.currentIndex];
        }
    }
}    
</script>
<style lang="scss">
.carousel {
    &__item {
        justify-content: center;
        align-items : center;
    }
}
</style>