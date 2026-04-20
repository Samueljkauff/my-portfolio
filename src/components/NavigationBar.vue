<template>
    <div @click="onExpandClick" :class="['flex flex-col justify-start h-screen bg-[#1b4332]', isOpen ? 'w-40 items-start' : 'w-15 items-center']">
        <div>
            <i class="pi pi-bars icon"></i>
        </div>
        <div>
            <i class="pi pi-code icon"> <p v-if="isOpen" class="inline"> Project</p></i>
        </div>
        <div>
            <i class="pi pi-user icon"><p v-if="isOpen" class="inline"> About</p></i>
        </div>
        <div>
            <i class="pi pi-comment icon"><p v-if="isOpen" class="inline"> Comment</p></i>
        </div>
        <div>
            <i class="pi pi-envelope icon"><p v-if="isOpen" class="inline"> Message</p></i>
        </div>
    </div>
</template>

<script lang="ts">
import 'primeicons/primeicons.css';

export default {
    data() {
        return {
            isOpen: false,
        }
    },
    methods: {
        onExpandClick() {
            this.isOpen = !this.isOpen;
        },
    }
}

</script>

<style>
    .icon {
        font-size: 25px;
        margin-top: 15px;
        color: #d8f3dc;
    }
</style>