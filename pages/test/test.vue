<template>
	<view>

	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
        onLoad() {
            this.printLog()
        },
		methods: {
            printLog() {
                let age = 20;
                console.log("----- number -----", age);

                let name = "小明";
                console.log('----- string -----', name);

                let isDone = false;
                console.log('---- boolean ----', isDone);

                var cars = new Array("Saab", "Volvo", "BMW");;
                console.log('---- 数组 -----', cars);

                let obj = {"name": "小明"};
                console.log('----- obj ---', obj);
                
                let tmp;
                console.log('---- 未定义 ----', tmp);
            }
		}
	}
</script>

<style>

</style>
