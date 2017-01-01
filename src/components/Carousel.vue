<template>
    <div class="container">
        <div class="">
            <div class="is-flex carousel__item">
                <img :src="currentItem.src"></img>
            </div>
        </div>
        <hr>
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
</template>
<script>
export default {
    name : 'vue-carousel',
    props: ['carouselItems'],
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