<template>
	<div class="field_usedTools" >
		<div :key="index" v-for="(tool, index) in toolsList" class="usedTools">
			<img :src="`https://cdn-istatics.herokuapp.com/static/icons/${tool.fileName}`">
			<p class="tool_name">{{ tool.label }}</p>
		</div>
	</div>
</template>

<script>

	// https://cdn-istatics.herokuapp.com/static/icons/${tool.fileName}

export default {
	name: 'Projects',

    props: {

        toolsList: Array
    }
}

</script>

<style scoped>

.field_usedTools {
	position: relative;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	width: 130px;
}


.usedTools {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 40px;
	height: 40px;
	margin: 10px 0;
}

.usedTools:hover .tool_name {
	display: inline-block;
}

.usedTools > img {
	width: 70%;
}

.tool_name {
	display: none;
	text-align: right;
	position: absolute;
	width: 120px;
	left: -125px;
}

</style>
