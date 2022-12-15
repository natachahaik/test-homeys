<template>

<section class="container">
<div class="container-header">
 <span class="success">
    <img :src="success" alt="icône success" class="success-icone"/>
    <h1>Modal Window</h1>
</span>

<div class="close">
    <img :src="close" alt="icône close" class="close-icone"/>
</div>
</div>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor fugiat nostrum ab aperiam molestiae maxime sit cupiditate, dolorem pariatur dolore maiores nobis. Unde reprehenderit placeat officiis aliquid, dicta beatae illum.</p>
</section>

</template>


<script lang="ts" setup>
import success from "@/assets/success.svg"
import close from "@/assets/close.svg"

</script>



<style lang="scss" scoped>

.container{
    background-color: #e4f7e8 ;
    width: 700px;
    height: 215px;
    margin: 40px;
    border:2px solid #3b793e ;
    border-radius: 16px;
    padding: 25px;
}

.container-header{
display: flex;
justify-content: space-between;
margin-bottom: 22px;
margin-left: 5px;
}

.success{
    display: flex;
    justify-content: flex-start;
    gap: 28px;
}

.success-icone {
    width: 40px;
}
.close{
    display: flex;
    justify-content: end;
}

.close-icone {
    width: 30px; 
}

p {
    font-size: 20px;
    margin-left: 65px;

}


</style>