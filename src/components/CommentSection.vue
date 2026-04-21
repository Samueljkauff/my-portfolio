<template>
  <div class="bg-[#000814] min-h-auto px-20 py-16">
    <h2 class="text-[#cad2c5] text-3xl font-bold mb-8">
      Leave a <span class="text-[#ffd60a]">comment</span>
    </h2>

    <div class="grid grid-cols-2 gap-8">
      <div class="flex flex-col gap-4">
        <input
          v-model="newName"
          type="text"
          placeholder="Your name"
          class="bg-transparent border border-[#ffd60a33] rounded-md px-4 py-2 text-[#cad2c5] placeholder-[#cad2c555] outline-none focus:border-[#ffd60a88]"
        />
        <textarea
          v-model="newMsg"
          rows="5"
          placeholder="Write something..."
          class="bg-transparent border border-[#ffd60a33] rounded-md px-4 py-2 text-[#cad2c5] placeholder-[#cad2c555] outline-none focus:border-[#ffd60a88] resize-none"
        />
        <button
          @click="postComment"
          class="w-fit border border-[#ffd60a] text-[#ffd60a] px-5 py-2 rounded-md hover:bg-[#ffd60a] hover:text-[#000814] transition-colors duration-200"
        >
          Post Comment
        </button>
      </div>

      <div class="flex flex-col gap-4">
        <p v-if="comments.length === 0" class="text-[#cad2c5] opacity-30 text-sm">No comments yet.</p>
        <div
          v-for="comment in comments"
          :key="comment.id"
          class="border border-[#ffd60a18] rounded-xl p-5 hover:border-[#ffd60a33] transition-colors duration-200"
        >
          <div class="flex items-center gap-3 mb-2">
            <div class="w-8 h-8 rounded-full bg-[#ffd60a22] border border-[#ffd60a44] flex items-center justify-center text-[#ffd60a] text-xs font-bold">
              {{ getInitials(comment.name) }}
            </div>
            <span class="text-[#cad2c5] text-sm font-semibold">{{ comment.name }}</span>
            <span class="text-[#cad2c5] opacity-30 text-xs ml-auto">{{ comment.time }}</span>
          </div>
          <p class="text-[#cad2c5] opacity-70 text-sm leading-relaxed pl-11">{{ comment.message }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      newName: '',
      newMsg: '',
      comments: [
        { id: 1, name: 'Alex Kim', message: 'Really clean portfolio! Love the dark theme and gold accents.', time: '2 hours ago' },
        { id: 2, name: 'Rachel Jones', message: 'Fellow Bellarmine grad — congrats on the upcoming graduation!', time: '5 hours ago' },
      ],
    }
  },
  methods: {
    getInitials(name: string) {
      return name.trim().split(' ').map((w: string) => w[0]).join('').toUpperCase().slice(0, 2) || '?'
    },
    postComment() {
      if (!this.newName.trim() || !this.newMsg.trim()) return
      this.comments.unshift({ id: Date.now(), name: this.newName.trim(), message: this.newMsg.trim(), time: 'Just now' })
      this.newName = ''
      this.newMsg = ''
    },
  },
}
</script>