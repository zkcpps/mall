<template>
    <div id="tab-bar">
     <slot></slot>
    </div>
</template>

<script>
import TabBarItem from './TabBarItem';

export default {  
    name: "TabBar",
    comonents: {
       TabBarItem
    }
}
</script>

<style>

  #tab-bar {
    position: fixed;
    height: 49px;
    background-color: #f6f6f6;
    display: flex;
    bottom: 0;
    left: 0;
    right: 0;
    box-shadow: 0px -1px 1px rgba(100, 100, 100, .1);
  }

</style> 