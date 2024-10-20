<template>
    <div class="container">
        <div class="title">
            <h5 >{{dataSet.titleSplide}}</h5>
            <a href="/">{{dataSet.anchorText}}</a>
        </div>
        <div class="splide-wrapper">
            <Splide id="thumbnail-carousel" :options="{pagination:false, perPage:dataSet.perPageValue,padding:'5%',gap:'1rem' }" aria-label="Thumbnail Carousel">
                <SplideSlide v-for="(image, index) in dataSet.imgSlide" :key="index">
                    <div class="img-container">
                        <img width="100%" :src="image" :alt="dataSet.titles[index]"/>
                    </div>
                    <p>{{ dataSet.titles[index] }}</p>
                </SplideSlide>
            </Splide>
        </div>
    </div>
    
</template>

<script setup lang="ts">
    interface dataSet {
        titleSplide: string;
        anchorText: String;
        perPageValue: Number;
        imgSlide: string[];
        titles: string[];
    }
    const props = defineProps<{dataSet:dataSet}>();

</script>
