<template>
    <section class="swiper-slide container mx-auto">
        <h2 class="text-4xl font-bold mt-24" id="work">My Work</h2>
        <div class="flex-1 flex mt-12">
            <ul class="w-1/3 flex flex-col gap-4">
                <template v-for="item in items">
                    <ListItem v-bind="item" />
                </template>
            </ul>
            <div class="w-2/3">

            </div>
        </div>
    </section>
</template>

<script>
import ListItem from '../components/ListItem';

export default {
    name: 'MyWork',
    components: [ListItem],
    data:{ 
        selected: 0,
        items: [
            title: 'Snow fox',
            description: 'Something',
        ],
    },
}
</script>
