<template>
    <div v-show="data.length > 0">
        <h3>Список рубрик</h3>
        <RubricaItemVue
            v-for="item in data"
            :item="item"
            :key="item.id"
        />
    </div>
</template>

<script>
import RubricaItemVue from './RubricaItem.vue';

export default {
    props: {
        data: {
            type: Array,
            required: true
        }
    },
    components: {
        RubricaItemVue,
    },
}
</script>

<style>
    
</style>