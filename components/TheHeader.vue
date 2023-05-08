<template>
  <div class="header">
    <NuxtLink class="login" :to="{ name: 'login' }"> Login </NuxtLink>
    <NuxtLink class="hover:text-blue-500 hover:underline" to="/"> <img class="logo_santanu" src="../src/img/logo-santanu.png" /> </NuxtLink>

      <!-- <NuxtLink class="hover:text-blue-500 hover:underline" to="/"> Home </NuxtLink> -->
      <NuxtLink class="about" :to="{ name: 'about' }"> Tentang Kami </NuxtLink>
      <!-- <NuxtLink class="hover:text-blue-500 hover:underline" :to="{ name: 'contact' }"> Contact </NuxtLink> -->
    
  </div>
</template>

<style>
.header {
  z-index: 20;
  width: 100%;
  padding: 2rem 4rem;
  position: absolute;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo_santanu {
  width: 80px;
  opacity: 70%;
}

.login {
  background-color: #4C4A4A;
  border-radius: 10px;
  text-align: center;
  width: 100px;
  height: 30px;
  color: white;
  font-size: 20px;
  padding: 5px;
  margin-bottom: 25px;
}

.login:hover {
  color: blue;
}

.about{
  background-color: #4C4A4A;
  border-radius: 10px;
  text-align: center;
  width: 100px;
  height: 30px;
  color: white;
  font-size: 10px;
  padding: 10px;
  margin-bottom: 25px;
}

.about:hover{
  color: blue;
}

</style>