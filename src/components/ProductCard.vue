<script setup>
import Dropdown from './Dropdown.vue';
defineProps({
    product: Object
})
</script>

<template>
    <a :href="product.href" class="group">
        <div class="aspect-w-1 aspect-h-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-w-7 xl:aspect-h-8">
            <img :src="product.imageSrc" :alt="product.imageAlt"
                class="h-full w-full object-cover object-center group-hover:opacity-75" />
        </div>
        <div class="flex justify-between">
            <div>
                <h3 class="mt-4 text-sm text-gray-700">{{ product.name }}</h3>
            </div>
            <div>
                <Dropdown />
            </div>
        </div>
    </a>
</template>
