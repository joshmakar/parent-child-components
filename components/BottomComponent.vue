<template>
    <div>
        {{someData}}

        <button type="button" @click="$emit('updateData')"></button>
    </div>
</template>

<script>
export default {
    props:{
        someData: {
            type: string
        }
    }
}
</script>