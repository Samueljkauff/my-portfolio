<template>
    <div :class="['sidebar flex flex-col justify-start h-screen bg-[#001d3d] items-center', isOpen ? 'w-45 items-start' : 'w-14']">
        <div @click="onExpandClick" class="nav-item">
            <i :class="isOpen ? 'pi pi-arrow-left icon' : 'pi pi-bars icon'"></i>
        </div>
        <div @click="scrollTo('about')" class="nav-item">
            <i class="pi pi-user icon"></i>
            <p :class="['label text-lg', isOpen ? 'label-enter' : 'label-exit']">About</p>
        </div>
        <div @click="scrollTo('projects')" class="nav-item">
            <i class="pi pi-code icon"></i>
            <p :class="['label text-lg', isOpen ? 'label-enter' : 'label-exit']">Projects</p>
        </div>
        <div @click="scrollTo('experience')" class="nav-item">
            <i class="pi pi-briefcase icon"></i>
            <p :class="['label text-lg', isOpen ? 'label-enter' : 'label-exit']">Experience</p>
        </div>
        <!-- <div @click="scrollTo('comments')" class="nav-item">
            <i class="pi pi-comment icon"></i>
            <p :class="['label text-lg', isOpen ? 'label-enter' : 'label-exit']">Comment</p>
        </div> -->
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
        scrollTo(id: string) {
            document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' });
        },
    }
}
</script>

<style>
    .sidebar {
        transition: width 0.3s ease;
        overflow: hidden;
    }

    .icon {
        font-size: 25px;
        color: #cad2c5;
        flex-shrink: 0;
        width: 25px;
        text-align: center;
        cursor: pointer;
    }

    .nav-item {
        display: flex;
        align-items: center;
        padding: 10px 14px;
        gap: 12px;
        width: 100%;
        transition: background 0.2s ease;
        border-radius: 6px;
    }

    .nav-item:hover {
        background: linear-gradient(to right, #52796f55, transparent);
        cursor: pointer;
    }

    .label {
        color: #cad2c5;
        white-space: nowrap;
    }

    .label-enter {
        animation: fadeIn 0.2s ease 0.15s both;
    }

    .label-exit {
        animation: fadeOut 0.15s ease both;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateX(-6px); }
        to   { opacity: 1; transform: translateX(0); }
    }

    @keyframes fadeOut {
        from { opacity: 1; transform: translateX(0); }
        to   { opacity: 0; transform: translateX(-6px); }
    }
</style>