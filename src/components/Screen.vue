<template>
    <div>
        <h1>{{ input }}</h1>
    </div>
</template>

<script>
    const component = {};

    component.name='Screen';
    component.props = {
        input: {
            type: String,
            default: ''
        }
    };

    export default component;
</script>