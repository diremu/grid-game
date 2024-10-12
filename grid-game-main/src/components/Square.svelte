<script>

</script>

<div class="square">
    <slot></slot>
</div>

<style>
    .square {
        background-color: rgb(223, 223, 177);
        width: 50px;
        height: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .green {
        background-color: rgb(16, 238, 16);
    }
</style>