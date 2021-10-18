<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: "Quote",
        props: ['quotes'],

    }
</script>

<style scoped>
    .panel-body {
        font-family: 'arizonia', cursive;
        font-size: 24px;
        color: #11164c;
        border: 2px solid rgba(0, 0, 0, 0.22);
        text-align: left;
        padding: 2px;
        margin: 3px;

    }

    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #ffe2e2;
    }

</style>