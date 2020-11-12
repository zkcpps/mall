<template>
    <div class="tab-bar-item" @click="clickItem" >
        <div v-if="!isActive"><slot name="itemIcon"></slot></div>
        <div v-else><slot name="itemIconActive"></slot></div>
        <div :style="activeStyle"><slot name="itemText"></slot></div>
    </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
      path: String,
      activeColor: {
          type: String,
          default: '#EC3A4E'
      }
  },
  data() {
      return {
          // isActive: true
      }
  },
  computed: {
      isActive() {
        return this.$route.path.includes(this.path);
      },
      activeStyle() {
          return this.activeColor && this.isActive  ? {color: this.activeColor} : {}
      }
  },
  methods: {
      clickItem() {
        this.$router.push(this.path);
      }
  }
}
</script>

<style>

.tab-bar-item {
   flex: 1;
   text-align: center;   
 }

 .tab-bar-item  img{
   width: 24px;
   height: 24px; 
   font-size: 10px;
 }

 .active {
     color: #f40;
 }

</style>