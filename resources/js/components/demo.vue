<template>
<div>

    <h1>{{ $t('hello') }}</h1>
</div>

</template>

<script>
export default {
    methods:{
        changeLanguage(obj){
            localStorage.setItem('language',obj.target.value)
        }
    }
}
</script>
