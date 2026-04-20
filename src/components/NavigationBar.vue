<template>
    <div :class="['flex flex-col justify-start h-screen bg-[#1b4332]', isOpen ? 'w-45 items-start' : 'w-15 items-start']">
        <div>
            <i @click="onExpandClick" :class="isOpen ? 'pi pi-arrow-left icon justify-end' : 'pi pi-bars icon'"></i>
        </div>
        <div>
            <i class="pi pi-code icon"> <p v-if="isOpen" class="inline text"> Projects</p></i>
        </div>
        <div>
            <i class="pi pi-user icon"><p v-if="isOpen" class="inline text"> About</p></i>
        </div>
        <div>
            <i class="pi pi-comment icon"><p v-if="isOpen" class="inline text"> Comment</p></i>
        </div>
        <div>
            <i class="pi pi-envelope icon"><p v-if="isOpen" class="inline text"> Message</p></i>
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
        margin-left: 15px;
        margin-right: 4px;
    }

    .text {
        margin-right: 2px;
    }
</style>