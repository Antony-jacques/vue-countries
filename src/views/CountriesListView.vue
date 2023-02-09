<template>
    <div>Countries List</div>
</template>
<script>
export default {
    name: 'countriesListView',
    mounted(){
        try {
            fetch('https://restcountries.com/v3.1/all')
            .then(response => response.json())
            .then(data => console.log(data))
        } catch (error){
           console.log(error); 
        }


    }


}


</script>