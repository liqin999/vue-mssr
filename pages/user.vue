<template>
    <div>
        <ul>
            <li>
                <nuxt-link to="/user">默认用户</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/user/1">用户1</nuxt-link>
            </li>
             <li>
                <nuxt-link to="/user/2">用户2</nuxt-link>
            </li>
      </ul>
        <nuxt-child/>
    </div>
</template>
<script>
export default {
    data(){
        return{

        }
    }
}
</script>