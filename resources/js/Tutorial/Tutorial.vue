<template>
    <div v-if="show" 
        class="fixed inset-0 z-50 w-full h-screen bg-black/50"
        @click="endTutorial"
    >
        <div class="h-full flex items-center justify-center">
            <div class="bg-white rounded max-w-md overflow-hidden shadow">
                <div class="bg-gray-100 p-4 font-semibold">
                    Heading
                </div>
                <div class="p-4">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit atque qui maxime molestiae magni, modi debitis sequi laudantium eius quod.
                </div>

            </div>
        </div>
    </div>

</template>

<script setup>
import { ref, defineEmits } from 'vue'

defineEmits(['update:show'])

const props = defineProps({
    steps: Array,
    show: Boolean
})

const endTutorial = () => {
    emit('update:show', false)
}



</script>