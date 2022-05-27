<template>
    <div id="gallery">
        <b-container fluid class="p-4 bg-dark">
            <b-jumbotron header="갤러리" lead="흘러가버린 추억을 이곳에서 확인하세요." class="text-light text-center my-5"></b-jumbotron>
            <b-row>
                <b-col cols="12" md="6" class="my-2"><b-img thumbnail fluid :src="require('../static/vpic1.jpg')" alt="Image 2"></b-img></b-col>
                <b-col cols="12" md="6" class="my-2"><b-img thumbnail fluid :src="require('../static/vpic2.jpg')" alt="Image 2"></b-img></b-col>
                <b-col cols="12" md="6" class="my-2"><b-img thumbnail fluid :src="require('../static/vpic3.jpg')" alt="Image 2"></b-img></b-col>
                <b-col cols="12" md="6" class="my-2"><b-img thumbnail fluid :src="require('../static/vpic4.jpg')" alt="Image 2"></b-img></b-col>
                <b-col cols="12" md="6" class="my-2"><b-img thumbnail fluid :src="require('../static/vpic5.jpg')" alt="Image 2"></b-img></b-col>
            </b-row>
        </b-container>
    </div>
</template>
<script>
export default {
    
}
</script>
<style>

</style>
