<template>
<div>
    <div>
        <div class="categories">
            <div v-for="item of listCategory" :key="item.uid" >
                <nuxt-link :to="localePath(item.img)">
                        <img class="categories__img" :src= "baseUrl + item.img" alt="">
                </nuxt-link>
            </div>
    </div>
    </div>
</div>
</template>

<script>
import MenuDefault from '~/components/shared/menu/MenuDefault';
import MenuDropdown from '~/components/shared/menu/MenuDropdown';
import MenuMega from '~/components/shared/menu/MenuMega';


export default {
    name: 'Categories',
    data() {
        return {
            baseUrl: "http://51.89.97.33:5500", 
            listCategory:[],
           
        };
    },
    async fetch(){
        this.listCategory = await fetch('http://51.89.97.33:5500/api/categories')
            .then(res => res.json());
    }
};
</script>

<style>
.categoriesText{
    font-size: 40px;
    text-align: center;
}
.categories{
    display: flex;
    flex: 0;
    overflow-x: auto;
    justify-content: space-between;
    flex-wrap: nowrap;
    
}
.categories::-webkit-scrollbar{
    display: none;
}
.categories > div {
    min-width: 150px;
    margin: 5px;
}
.categories__img{
    object-fit: contain;
    width: 100%;
    border: 2px solid;
    border-color: rgb(8, 8, 8) green;
    border-radius: 10px;
    box-shadow: 4px 4px 20px rgb(228, 255, 246);
}
</style>