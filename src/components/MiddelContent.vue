<template>
 <div>
   <div id="element2">
    <div id="element1">ploum ploum</div>
</div>
 </div>
</template>
<script>
export default {
    name: 'MiddelContent',
}
</script>
<style scoped>
#element1 {
    position:absolute;
    background-color:#00CCFF; /* bleu ciel */
    width:50px;
    height:50px;
    text-align:center;
    top:55px;
    left:42px;
    }
#element2 {
    position:absolute;
    background-color:#CC66CC; /* violet */
    width:100px;
    height:100px;
    text-align:center;
    top:50px;
    left:70px;
    }
</style>