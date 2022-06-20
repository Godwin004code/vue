
<template>
    <div class="backdrop">
        <div class="modal">
            <h2>{{ header }}</h2>
            <p>{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['header', 'text']
}

</script>
<style>
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: red;
}
.backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, .5);
}
</style>