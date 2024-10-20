<template>
    <div class="new-main-container">
        <div class="main-container":style="{ backgroundImage: 'url(' + bannerImg + ')'}">
            <div class="main-content">
                <h3>{{bannerTitle}}</h3>
                <p>
                    {{bannerText}}
                </p>
                <a class="btn" :href="bannerLink">SIGUE LA ACCIÓN</a>
            </div>
        </div>
    <</div>
</template>
<script setup>
const props =defineProps({
        bannerImg: String,
        bannerTitle: String,
        bannerText: String,
        bannerLink: String
    })
</script>