<template>
    <div  class="p-4 m-2 bg-slate-400 flex justify-between">
        <div>Нзвание рубрики: <strong>{{item.title}}</strong> - ({{item.count}})</div>
        <button>
            Открыть
        </button>
    </div>
</template>

<script>
export default {
    props: {
        item: {
            type: Object,
        },
    },
}
</script>

<style>
    
</style>