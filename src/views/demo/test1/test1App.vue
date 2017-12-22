<template>

<div id="app">
	<h1 v-text="title"></h1>
	<h2 class="h2-red">red</h2>
	<table class="table">
		<tr>
			<th>ID</th>
			<th>name</th>
			<th>url</th>
			<th>number</th>
		</tr>
		<tr v-for="item in list">
			<td v-text="item.id"></td>
			<td v-text="item.name"></td>
			<td v-text="item.url"></td>
			<td>{{ item.number | currency }}</td>
		</tr>
	</table>
	<table>
		<tr>
			<th>ID</th>
			<th>name</th>
			<th>url</th>
		</tr>
		<tr v-for="item in list">
			<td v-text="item.id"></td>
			<td v-text="item.name"></td>
			<td v-text="item.url"></td>
		</tr>
	</table>
</div>

</template>

<script>

import Lib from 'assets/js/Lib';

export default {
  	data() {
		return {
	    	'title': '这是一个标题',
			'list':[
				{
					'id': 0,
					'name': 'name1',
					'url': '../name1.html',
					'number': 111.1122
				},{
					'id': 1,
					'name': 'name2',
					'url': '../name2.html',
					'number': 222.2255
				},{
					'id': 2,
					'name': 'name3',
					'url': '../name3.html',
					'number': 333.3388
				},{
					'id': 3,
					'name': 'name4',
					'url': '../name4.html',
					'number': 444.1
				},{
					'id': 4,
					'name': 'name5',
					'url': '../name5.html',
					'number': 555
				}
			]
	    }
	}
}

</script>

<style lang="less">

h1 {
	color: red;
}
.table{
	th {
		color: blue;
	}
	td {
		color: gray;
	}
}


</style>
