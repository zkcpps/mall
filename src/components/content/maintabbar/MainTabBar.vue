<template>
   <tab-bar>
      <tab-bar-item path='/home'>
      <template v-slot:itemIcon>
         <img src="@/assets/img/tabbar/home.svg" alt="">
      </template>
       <template v-slot:itemIconActive>
         <img src="@/assets/img/tabbar/home-active.svg" alt="">
       </template>
       <template v-slot:itemText>
         <div>首页</div>
       </template>
      </tab-bar-item>
      <tab-bar-item path='/category'>
         <template v-slot:itemIcon>
         <img src="@/assets/img/tabbar/category.svg" alt="">
      </template>
       <template v-slot:itemIconActive>
         <img src="@/assets/img/tabbar/category-active.svg" alt="">
       </template>
       <template v-slot:itemText>
         <div>分类</div> 
       </template>
      </tab-bar-item>
      <tab-bar-item path='/cart'>
       <template v-slot:itemIcon>
        <img src="@/assets/img/tabbar/cart.svg" alt="">
      </template>
       <template v-slot:itemIconActive>
         <img src="@/assets/img/tabbar/cart-active.svg" alt="">
       </template>
       <template v-slot:itemText>
         <div>购物车</div>
       </template>
      </tab-bar-item>
      <tab-bar-item path='/profile'> 
       <template v-slot:itemIcon>
         <img src="@/assets/img/tabbar/profile.svg" alt="">
      </template>
       <template v-slot:itemIconActive>
         <img src="@/assets/img/tabbar/profile-active.svg" alt="">
       </template>  
       <template v-slot:itemText> 
         <div>我的</div>
       </template>
      </tab-bar-item>  
   </tab-bar>  
</template>
  
<script>

import TabBar from '@/components/common/tabbar/TabBar'
import TabBarItem from '@/components/common/tabbar/TabBarItem'

export default {
    name: 'MainTabBar',
    components: {
      TabBar,
      TabBarItem
    }
}
</script>

<style>
  
</style>