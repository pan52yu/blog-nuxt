<script lang="ts" setup>
import {subNavLinks} from '@/site.config'

const route = useRoute()

const {path} = route

const router = useRouter()
</script>

<template>
    <ul class="flex gap-4 mb-8">
        <li
            v-for="(item) in subNavLinks" :key="item.path"
            :class="path === item.path ? 'text-deep font-bold' : 'deep-hover'"
            class="cursor-pointer "
            @click="router.push(item.path)"
        >
            <span class="text-title"> {{ item.title }}</span>
        </li>
    </ul>
</template>
