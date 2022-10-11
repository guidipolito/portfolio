<template>
    <div>
        <div @click="handleClick" class="bg-gray-900 p-2 text-sm transition-all hover:scale-105">{{value}}</div>
        <input readonly ref="input" class="w-0 h-0 hidden" v-bind:value="value" />
        <small class="text-sm text-green-300" v-show="copied">Copied</small>
    </div>
</template>

<script>
export default {
    name: 'CopyArea',
    props: ['value'],
    data(){
        return { copied: false, }
    },
    methods: {
        handleClick(){
            let input = this.$refs.input
            input.select();
            input.setSelectionRange(0, 99999); //
            navigator.clipboard.writeText(input.value);
            this.copied = true
            setTimeout(()=>this.copied = false, 2000)
        }
    }
}
</script>
