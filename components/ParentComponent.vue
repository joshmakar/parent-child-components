<template>
    <div>
        <top-left-component :some-data="someData" @updateData="fetchData"></top-left-component>

        <bottom-component :some-data="someData" @updateData="fetchData"></bottom-component>
    </div>
</template>

<script>
import TopLeftComponent from 'TopLeftComponent';
import BottomComponent from 'BottomComponent';

export default {
    components: {
        'top-left-component': TopLeftComponent,
        'bottom-component': BottomComponent,
    },

    data() {
        return {
            someData: ''
        }
    },

    methods: {
        fetchTheData() {
            //Make the call
            someData = 'blah blah blah';
        }
    },
}
</script>