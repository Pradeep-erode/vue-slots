<template>
    <div>
        {{ vertu }}
        <p>{{ content }}</p>
    </div>

    <slot></slot>

    <div>
        <!-- named slot -->
        <slot name="header"></slot>

        <!-- we can give default value if content not getting from parent  -->
        <slot name="footer">Default value</slot>
    </div>

</template>

<script>
export default {
    name: 'apple-fruit',
    props: ['vertu', 'content']
}
</script>

<style>
div{
    color: red;
}
</style>