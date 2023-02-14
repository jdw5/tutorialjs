<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8 flex flex-col">
                
                <div class="flex justify-between">
                    <div>
                        Breadcrumbs
                    </div>
                    <div class="flex gap-x-2">
                        <button class="p-1 text-sm text-indigo-500">
                            Add
                        </button>
                        <button class="p-1 text-sm text-indigo-500">
                            Delete
                        </button>
                        <button @click="initiateTutorial" class="p-1 text-sm text-indigo-500">
                            Tutorial
                        </button>
                    </div>
                </div>
                <div class="flex-grow py-12">
                    <div class="w-24 bg-indigo-500 h-full">

                    </div>
                    <div class="max-w-4xl aspect-video h-full bg-white mx-auto rounded shadow">

                    </div>
                    
                </div>
                <div class="bg-white h-48 py-4">
                    
                </div>
            </div>
        </div>

        <Tutorial 
            :steps="steps"
            :show="showTutorial"
        />
    </AuthenticatedLayout>
</template>


<script setup>
import { ref, reactive } from 'vue'
import Tutorial from '@/Tutorial/Tutorial.vue'
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

let showTutorial = ref(false);

const initiateTutorial = () => {
    showTutorial.value = true
}

const steps = reactive([
    {
        id: 0,
        title: 'Delete via this method or whatever',
        element: null
    }, {
        id: 1,
        element: null,
    }
])

</script>