<template>
   <div class="row cover-wrapper align-items-center p-5">
       <div class="col-md-7">
           <h2 class="cover-title">Every purchase will be made with pleasure</h2>
           <p class="cover-desc">Lorem ipsum dolor sit amet consectetur Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda, et?</p>
           <input class="cover-input" type="text" placeholder="Start shopping">
       </div>
       <div class="col-md-5">
           <img class="cover-img" src="../assets/images/cover_2.svg" alt="">
       </div>
   </div>
</template>

<style>
.cover-wrapper{
    height: 60vh;
}
.cover-title,.cover-desc{
    margin-bottom: 25px;
    color: #212121;
}
.cover-img{
    width: 75%;
    object-fit: cover;
    max-height: 60vh;
}
.cover-desc{
    width: 80%;
    font-size: 1rem;
}
.cover-input{
    width: 50%;
    border: 1px solid #6c7a89;
    border-radius: 5px;
    padding: 10px 20px;
}


@media (max-width: 767px) {
  .cover-wrapper{
      height: 100vh;
      padding: 20px !important;
      flex-direction: row-reverse !important;
  }


.cover-img{
    display: none;
}
  .cover-desc,
  .cover-title,
  .cover-input{
      width: 100%;
  }
  
}
</style>