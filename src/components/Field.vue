<template>
  <div> 
    <div class="field" v-on:click='click'>
        {{value}}
    </div>  
</div>
</template>

<script>
export default {
    props: ['value'],
    methods: {
        click(){
            this.$emit('click')
        }
    },

}
</script>

<style>
.field{
    width: 100px;
    height: 100px;
    border: 3px solid black;
    margin: 1px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.field:hover{
    cursor: pointer;
}

</style>