<template>
<div>

    <KemSelect v-model="multipleValue" multiple :options="options"></KemSelect>
    <KemSelect v-model="value" :options="options"></KemSelect>
    <KemSelect v-model="value" :options="options">
        <template slot-scope="{scope}">
            <span style="float: left">{{ scope.label }}</span>
            <span style="float: right; color: #8492a6; font-size: 13px">{{ scope.value }}</span>
        </template>
    </KemSelect>
    <KemInputNumber v-model="number" ></KemInputNumber>

</div>
</template>

<script>
export default {
    name: "Form",
    data() {
        return {
            multipleValue:[],
            value:'',
            number:3,
            options: [
                {
                    value: 'Beijing',
                    label: '北京'
                }, {
                    value: 'Shanghai',
                    label: '上海'
                }, {
                    value: 'Nanjing',
                    label: '南京'
                }, {
                    value: 'Chengdu',
                    label: '成都'
                }, {
                    value: 'Shenzhen',
                    label: '深圳'
                }, {
                    value: 'Guangzhou',
                    label: '广州'
                }
            ]
        }
    },
}
</script>

<style scoped>

</style>
