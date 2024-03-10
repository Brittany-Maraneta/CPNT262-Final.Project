<template>
<div class="hamburger-menu">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
  </div>
</template>

<style lang="scss" scoped>
.bar {  
  width: 30px;   
  height: 3.5px;   
  background-color: white; 
  margin: 4px 0;   
 } 

 .hamburger-menu { 
   display: flex;
   flex-direction: column;   
   cursor: pointer; 
 }


</style>