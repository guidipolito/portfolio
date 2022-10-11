<template>
    <div class="w-full md:w-1/3 p-5">
        <div class="rounded-md border border-blue-800 w-full bg-black/25 p-5 h-full">
            <slot/>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: [ 'children' ]
}
</script>
