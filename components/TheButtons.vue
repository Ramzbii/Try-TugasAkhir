<template>
    <div class="main-buttons">
        <!-- <NuxtLink class="hover:text-blue-500 hover:underline"  to="/"> Home </NuxtLink> -->
        <NuxtLink class="button" :to="{ name: 'legend' }  ">
            <div class="bulat">
                <img class="logo-button-legend" src="../src/img/legend.png">    
            </div>
            <p class="tulisan">Legend</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'point' }">
            <div class="bulat">
                <img class="logo-button-point" src="../src/img/point.png">    
            </div>
            <p class="tulisan">Point</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'rain' }">
            <div class="bulat">
                <img class="logo-button-rain" src="../src/img/rain.png">    
            </div>

            <p class="tulisan">Rain</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'flood' }">
            <div class="bulat">
                <img class="logo-button-flood" src="../src/img/flood.png">    
            </div>
            <p class="tulisan">Flood</p>
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'gsmap' }" >
            <div class="bulat">
                <img class="logo-button-gsmap" src="../src/img/satelite.png">    
            </div>
            <p class="tulisan">Satelite</p> 
        </NuxtLink>
        <NuxtLink class="button" :to="{ name: 'qpe' }">
            <div class="bulat">
                <img class="logo-button-dbz" src="../src/img/dbz.png">       
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

.bulat {
    width: 40px;
    height: 40px;
    background: #4C4A4A;
    opacity: 75%;
    border-radius: 100%;
    text-align: right;
    position: relative;
}

.button:hover .tulisan {
    background-color:#4C4A4A;
    border-radius: 10px;
    opacity: 70%;
}
.logo-button-legend{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
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


.logo-button-point{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.logo-button-rain{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.logo-button-flood{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.logo-button-gsmap{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

.logo-button-dbz{
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
}

/* .logo-button-dbz{
    position: absolute;
    right: 6px;
    margin-top: 10px;
    width: 15%;
} */

.logo-button-dbz:hover{

}


.button p {
    font-size: 15px;
    float: right;
    padding: 10px 15px;
    color: white;
    text-shadow: 2px 2px 3px #4C4A4A;
    position: relative;
}

/* .bulat:hover {
   opacity: 20%;
} */

.button p:hover {
  color: #4C4A4A;
}

</style>