<template>
    <div>
        <input type="file" accept="image/*" class="hidden" ref="file" @change="change">
        <img src="src" alt="Avatar" class="avatar">
        <button @click="browse()">Browse</button>


    </div>
</template>

<script>


    export default {
        data() {
            return {
                src: null
            }
        },
        props: {
            value: File
        },
        methods: {
            browse() {
                this.$refs.file.click();
            },
            change(e) {
                this.$emit('input', e.target.files[0]);
                let reader = new FileReader();
                reader.readAsDataURL(e.target.files[0]);

                reader.onload = (e) => {
                    this.src = e.target.result;
                }
            }
        }
    }

</script>

<style>
    .avatar {
        height: 24px;
        width: 24px;
        border-radius: 50%;
        object-fit: cover;
    }

    .hidden {
        visibility: hidden;
    }

</style>