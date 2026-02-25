<template>
    <div class="contact" id="contact">
        <div class="con">
            <h2>Contact Us</h2>

            <form @submit.prevent="handleSubmit">
                <input type="text" placeholder="Enter your Name" v-model="form.name" :class="{ error: errors.name }" />

                <input type="email" placeholder="Enter your Email" v-model="form.email"
                    :class="{ error: errors.email }" />

                <textarea placeholder="Enter your message" v-model="form.message"
                    :class="{ error: errors.message }"></textarea>

                <button type="submit" class="btn btn-primary">
                    Send Message
                </button>
                <div class="toast-container position-fixed bottom-0 end-0 p-3">
                    <div ref="toastRef" class="toast" role="alert" aria-live="assertive" aria-atomic="true">
                        <div class="toast-header">
                            <img src="../assets/logo.png" class="rounded me-2" alt="logo" />
                            <strong class="me-auto">ABHI</strong>
                            <small>Just now</small>
                            <button type="button" class="btn-close" data-bs-dismiss="toast"></button>
                        </div>
                        <div class="toast-body">
                            Thank you for contacting us! We will get back to you shortly.
                        </div>
                    </div>
                </div>

            </form>
        </div>
    </div>
</template>
<script setup>
import { reactive, ref } from 'vue'

const form = reactive({
    name: '',
    email: '',
    message: ''
})

const errors = reactive({
    name: false,
    email: false,
    message: false
})

const toastRef = ref(null)

const handleSubmit = () => {
    errors.name = !form.name.trim()
    errors.email = !form.email.trim()
    errors.message = !form.message.trim()

    if (errors.name || errors.email || errors.message) return

    const toast = bootstrap.Toast.getOrCreateInstance(toastRef.value)
    toast.show()

    form.name = ''
    form.email = ''
    form.message = ''
}
</script>
<style>
.contact {
    margin-top: 80px;
    text-align: center;
    display: flex;
    justify-content: center;
}

.con {
    width: 500px;
    padding: 30px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
}

form {
    display: flex;
    flex-direction: column;

    margin: 20px auto;
    gap: 15px;
}

input,
textarea {
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

input:focus,
textarea:focus {
    outline: none;
    border-color: #0b5ed7;
    box-shadow: 0 0 5px #0b5ed7;
}

.error {
    border-color: red !important;
    box-shadow: 0 0 5px red !important;
}

.toast-header img {
    width: 20px;
    height: 20px;
}

@media (max-width:600px) {
    .contact {
        margin-top: 80px;
        text-align: center;
        display: flex;
        justify-content: center;
    }

    .con {
        width: 100%;
        padding: 30px;
        box-shadow: none;

    }
}
</style>