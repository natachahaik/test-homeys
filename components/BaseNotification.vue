<template>

<section
    class="container" 
    :class="{ 
        success: variant === 'success',
        warning: variant === 'warning',
        danger: variant === 'danger',
        info: variant === 'info' 
    }"
>

    <div class="container-header">
        <span class="header-success">
            <img :src="srcComputed" alt="icon" class="success-icon"/>
            <h1>{{ title }}</h1> 
        </span> 
        <div class="close">
            <img :src="close" alt="icône close" class="close-icon"/>
        </div>
    </div>

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor fugiat nostrum ab aperiam molestiae maxime sit cupiditate, dolorem pariatur dolore maiores nobis. Unde reprehenderit placeat officiis aliquid, dicta beatae illum.</p>
</section>

</template>


<script>
import success from "@/assets/success.svg";
import warning from "@/assets/warning.svg";
import danger from "@/assets/danger.svg";
import info from "@/assets/info.svg"
import close from "@/assets/close.svg"

export default {
    name: 'BaseNotification',
    props: {
        variant: String,
        title: String
    },
    computed: {
        close: () => close,
        srcComputed() {
            if(this.variant === "success") {
                return success
            }
            if(this.variant === "info") {
                return info
            } 
            if(this.variant === "danger") {
                return danger
            }
            if(this.variant === "warning") {
                return warning
            }
            return success 
        }
    }
}
</script>

<style lang="scss" scoped>
.container{
    width: 700px;
    height: 215px;
    margin: 40px;
    border:2px solid ;
    border-radius: 16px;
    padding: 25px;
    &.success {
         background-color: #e4f7e8; 
         border: #3b793e;
    }
    &.warning {
        background-color: #f7f2e4;
        border: #d4c296;
    }
    &.danger {
        background-color: #f7e4e4;
        border: #b04040;
    }
    &.info {
        background-color: #e4e9f7;
        border: #2d52b1;
    }
}

.container-header{
    display: flex;
    justify-content: space-between;
    margin-bottom: 22px;
    margin-left: 5px;
}

.header-success{
    display: flex;
    justify-content: flex-start;
    gap: 28px;
}

.success-icon{
    width: 40px;
}
.close{
    display: flex;
    justify-content: end;
}

.close-icon{
    width: 30px; 
}

p{
    font-size: 20px;
    margin-left: 65px;
}
</style>