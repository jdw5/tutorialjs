<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
import { ref, reactive } from 'vue'
import Tutorial from '../Tutorial/Tutorial.vue';
</script>

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
                        <button>
                            Add
                        </button>
                        <button>
                            Delete
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
        
        />
    </AuthenticatedLayout>
</template>


<script setup>
import { ref, reactive } from 'vue'
import Tutorial from '@/Tutorial/Tutorial.vue'

const showTutorial = ref(false);

const initiateTutorial = () => {
    showTutorial = true
}

const steps = reactive([
    {
        id: 0,
        title: 'Delete via this method or whatever'
        element: null
    }, {
        id: 1,
        element: null,
    }
])

</script>