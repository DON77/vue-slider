<template>
    <header>
        <v-toolbar app>
            <v-toolbar-title v-text='title'>
            </v-toolbar-title>
            <v-spacer>
                <nav>
                    <ul class='flex-container flex-end'>
                        <li 
                        v-for='(item, index) in items' 
                        :key='index' 
                        class='flex-item'>
                            <router-link :to='item.link'>{{item.title}}</router-link>
                        </li>
                    </ul>         
                </nav> 
            </v-spacer>
        </v-toolbar>
        <my-slider />
    </header>
</template>

<script>
import Slider from './Slider'

export default {
  data () {
    return {
      title: 'vue-slider',
      items: [
        {title: 'Home', link: '/'},
        {title: 'About Us', link: '/about'},
        {title: 'Contact Us', link: '/contact'}
      ]
    }
  },
  name: 'Header',
  components: {
    'my-slider': Slider
  }
}
</script>

<style scoped lang='stylus'>
    .flex-container 
        padding 0
        margin 0
        list-style none
        display flex
    
    .flex-item 
        padding 5px
        margin 5px
        color white
        font-weight bold
        font-size 1em
        text-align center
        text-transform uppercase
    
    .flex-end 
        justify-content flex-end
    
    .flex-end 
        li 
            background #54b883
    
    .flex-end 
        li:hover 
            background #36495d
    
    .flex-end 
        li 
            a 
                color #fff
                text-decoration none
</style>