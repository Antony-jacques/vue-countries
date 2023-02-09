<template>
    <div>
        <div class="name">
            Country: {{ country.name.official}}
        </div>
        <div class="image-wrapper">
            <img :src=country.flags.svg alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'CountryItem',
    props: {
        country: Object
    }
}

</script>

<style>
img {
    width:200px
}

</style>