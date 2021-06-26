<template>
    <div class="row">
        <div class="col-md-12 border">
            <div class="king-nav d-flex justify-content-between align-items-center">
                <div class="logo"><Logo/></div>
               <i class="bi bi-list"></i>
                <div class="links">
                   <div class="burger-menu">
                        <BurgerMenu/>
                   </div>
                    <ul class="d-flex nav-links-wrapper align-items-center">
                        <li class="navlinks"><NuxtLink to="/accounts" class="nav-link">Account</NuxtLink></li>
                        <li class="navlinks"><NuxtLink to="/orders" class="nav-link">Orders</NuxtLink></li>
                        <li class="navlinks"><NuxtLink to="/cart" class="nav-link">Cart</NuxtLink></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.burger-menu{
    display: none;
}
.king-nav{
    padding: 10px 20px;
  
}
.nav-links-wrapper{
    list-style: none;
    margin: 0px !important;
}

@media (max-width: 767px) {
  .nav-links-wrapper{
      display: none !important;
  }

  .burger-menu{
      display: block;
  }
  
}
</style>