<template>
  <div class="header">
  <!-- <div class="header">
    <ul class="menu">
    <li class="menuItem">>Home</li>
    <li class="menuItem">Profile</li>
    <li class="menuItem">>About</li> 
    <li class="menuItem">Contacts</li>
    </ul>
      <button class="hamburger">
        <i>
          <Icon class="menuicon" name="ic:baseline-dehaze"/>
        </i>
        <i>
          <Icon class="closeicon" name="ic:baseline-cancel"/>
        </i>
      </button> -->
    
    
    <NuxtLink class="login" :to="{ name: 'login' }"> Login </NuxtLink>
    <NuxtLink to="/"> <img class="logo_santanu" src="../src/img/logo-santanu.png" /> </NuxtLink>
    <NuxtLink class="about" :to="{ name: 'about' }"> Tentang Kami </NuxtLink>
    
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

/* .menuItem {
  display: block;
  margin: 2rem 4rem;
  font-size: 1.8rem;
  color: white;
  text-decoration: none;
}

.menuItem:hover {
  text-decoration: underline;
}

.hamburger {
  position: fixed;
  z-index: 100;
  top: 1rem;
  right: 1rem;
  padding: 4px;
  border: black solid 1px;
  background: white;
  cursor: pointer;
}

.closeIcon {
  display: none;
}

.menu {
  position: fixed;
  transform: translateY(-100%);
  transition: transform 0.2s;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 99;
  background: black;
  color: white;
  list-style: none;
  padding-top: 4rem;
}

.showMenu {
  transform: translateY(0);
} */
</style>