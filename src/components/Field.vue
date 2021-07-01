<template>
  <div> 
    <div class="field">
        <p class="cross">X</p>
        <p class="circle">O</p>
    </div>  
</div>
</template>

<script>
export default {

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

.cross{
    display: none;
    font-size: 5rem;
}

.circle{
     display: none;
    font-size: 5rem;
}




</style>