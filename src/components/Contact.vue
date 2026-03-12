<template lang="html">
    <div class="relative py-24 overflow-hidden bg-gradient-to-r from-blue-900/50 to-cyan-900/50" id="contact">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl font-bold text-white mb-6 tracking-tight">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-cyan-500">Contact
                        Me</span>
                </h2>
                <p class="mt-4 text-blue-300 max-w-3xl mx-auto text-lg leading-relaxed">
                    If you have any questions or would like to work together, feel free to reach out to me through the
                    contact form below.
                </p>
            </div>
            <div class="max-w-md mx-auto px-4 sm:px-0" data-aos="fade-up" data-aos-delay="200">
                <form @submit.prevent="handleSubmit" class="bg-gray-800/80 backdrop-blur-sm rounded-xl p-8 shadow-xl border border-gray-700/50">
                    <div class="mb-5">
                        <label for="name" class="block text-sm font-medium text-gray-300 mb-2">Name</label>
                        <input type="text" id="name" v-model="form.name" name="name" required
                            class="w-full px-4 py-3 rounded-lg bg-gray-700/50 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all duration-300 text-white placeholder-gray-400">
                    </div>
                    <div class="mb-5">
                        <label for="email" class="block text-sm font-medium text-gray-300 mb-2">Email</label>
                        <input type="email" id="email" v-model="form.email" name="email" required
                            class="w-full px-4 py-3 rounded-lg bg-gray-700/50 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all duration-300 text-white placeholder-gray-400">
                    </div>
                    <div class="mb-6">
                        <label for="message" class="block text-sm font-medium text-gray-300 mb-2">Message</label>
                        <textarea id="message" v-model="form.message" name="message" rows="4" required
                            class="w-full px-4 py-3 rounded-lg bg-gray-700/50 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all duration-300 text-white placeholder-gray-400 resize-none"></textarea>
                    </div>
                    <div class="flex flex-col sm:flex-row gap-3">
                        <button type="submit" @click.prevent="sendViaEmail"
                            class="flex-1 px-6 py-3 bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white rounded-lg font-medium transition-all duration-300 hover:shadow-lg hover:shadow-blue-500/30 hover:scale-105 text-center">
                            Send Email
                        </button>
                        <button type="submit" @click.prevent="sendViaTelegram"
                            class="flex-1 px-6 py-3 bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white rounded-lg font-medium transition-all duration-300 hover:shadow-lg hover:shadow-blue-500/30 hover:scale-105 text-center">
                            Send Telegram
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            form: {
                name: '',
                email: '',
                message: ''
            },
            myEmail: 'sophorsdoeun@gmail.com',
            telegramUsername: 'DoeunSoPhors'
        }
    },
    methods: {
        sendViaEmail() {
            const subject = `Contact from ${this.form.name}`;
            const body = `Name: ${this.form.name}%0D%0AEmail: ${this.form.email}%0D%0AMessage: ${this.form.message}`;
            window.location.href = `mailto:${this.myEmail}?subject=${subject}&body=${body}`;
        },
        sendViaTelegram() {
            const text = `Hello! My name is ${this.form.name}.%0D%0AEmail: ${this.form.email}%0D%0AMessage: ${this.form.message}`;
            window.open(`https://t.me/${this.telegramUsername}?text=${text}`, '_blank');
        },
        handleSubmit() {
            // Default handler, not used since we use specific send methods
        }
    }
}
</script>
<style lang="">

</style>