<template>
    <li class="rounded-md border border-blue-800 w-full bg-black/25 p-5 transition-all hover:shadow-md shadow-blue-600/50" v-bind:class="{'shadow-xl shadow-blue-500/50': selected}"> 
        {{ title ?? '' }}
        {{ description ?? '' }}
    </li>
</template>

<script>
export default {
    name: 'ListItem',
    props: ['title', 'description', 'technologies', 'selected'],
}
</script>
