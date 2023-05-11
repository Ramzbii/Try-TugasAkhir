<template>
    <div class="main-buttons">
        <!-- <NuxtLink class="hover:text-blue-500 hover:underline"  to="/"> Home </NuxtLink> -->
        <NuxtLink class="button" :to="{ name: 'areaPantauan' }  ">
            <div class="button-circle">
                <Icon class="button-logo" name="ic:baseline-location-on"/> 
            </div>
            <p class="tulisan">Area Pantauan</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'history' }">
            <div class="button-circle">
                <Icon class="button-logo" name="ic:baseline-history"/>
            </div>
            <p class="tulisan">History</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'prediksi' }">
            <div class="button-circle">
                <Icon class="button-logo" name="ic:baseline-batch-prediction"/>
            </div>
            <p class="tulisan">Prediksi</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'gsmap' }" >
            <div class="button-circle">
                <Icon class="button-logo" name="ic:baseline-satellite-alt"/>
            </div>
            <p class="tulisan">Satelite</p> 
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'qpe' }">
            <div class="button-circle">
               <Icon class="button-logo" name="ic:baseline-area-chart"/>
            </div>
            <p class="tulisan">QPE</p>
        </NuxtLink>
    </div>
</template>

<script setup>
</script>

<style>
.main-buttons {
    z-index: 10;
    position: absolute;
    display: flex;
    flex-direction: column;
    margin-top: 120px;
    justify-content: flex-end;
    right: 2%;
    
}
.button {
    width: 100%;
    height: 50px;
    /* background: #4C4A4A; */
    border-radius: 100%;
    margin: 5px;
    display: flex;
    flex-direction: row-reverse;
    justify-content: right;
    align-items: center;
}
.button-circle {
    width: 40px;
    height: 40px;
    background: #4C4A4A;
    opacity: 75%;
    border-radius: 100%;
    text-align: right;
    position: relative;
}
.button-logo{
    width: 25px;
    height: 25px;
    color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);   
}
.button:hover .tulisan {
    background-color:#4C4A4A;
    border-radius: 10px;
    opacity: 70%;
}

/* .logo-button-legend:hover{
  animation-name: spin;
  animation-duration: 1000ms;
  animation-iteration-count: infinite;
  animation-timing-function: linear; 
}

@keyframes spin {
    from {
        transform:rotate(0deg);
    }
    to {
        transform:rotate(360deg);
    }
} */



.button p {
    font-size: 15px;
    float: right;
    padding: 10px 15px;
    color: white;
    text-shadow: 2px 2px 3px #4C4A4A;
    position: relative;
}

</style>