<template>
<div class="container bg-gray-800 w-full lg:max-w-full h-screen ">
	<h1 class="flex justify-center text-2xl text-white bg-gray-700 py-2">Crud App </h1>	

	<div class="pt-14">
		<div class="overflow-x-auto relative shadow-md">
				 <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
			        <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
			            <tr>
			                <th scope="col" class="py-3 px-6">
			                    Product name
			                </th>
			                <th scope="col" class="py-3 px-6">
			                    Color
			                </th>
			                <th scope="col" class="py-3 px-6">
			                    Category
			                </th>
			                <th scope="col" class="py-3 px-6">
			                    Price
			                </th>
			                <th scope="col" class="py-3 px-6">
			                    <span class="sr-only">Edit</span>
			                </th>
			            </tr>
			        </thead>
		        <tbody>
		            <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600" v-for="item in items" :key="item.id">
		                <th class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
		                    {{item.name}}
		                </th>
		                <td class="py-4 px-6">
		                   {{item.phoneNumber}}
		                </td>
		                <td class="py-4 px-6">
		                    {{item.status}}
		                </td>
		                <td class="py-4 px-6">
		                    {{item.email}}
		                </td>
		                <td class="py-4 px-6 text-right">
		                    <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline" @click="deleteItems(item)">Delete</a>
		                </td>
		            </tr>
		        </tbody>
	    </table>
		</div>
	</div>
</div>

</template>

<script setup>
import { ref } from 'vue'


const items = ref([
	{
		id: 1,
		name: 'iskat badmus',
		phoneNumber: '09084432562',
		status: 'active',
		email: 'iskat@gmail.com'
	},
	{
		id: 2,
		name: 'ade lawal',
		phoneNumber: '09084432562',
		status: 'inactive',
		email: 'ade@gmail.com'
	},
	{
		id: 3,
		name: 'sola berrin',
		phoneNumber: '09084432562',
		status: 'active',
		email: 'sola@gmail.com'
	},
	{
		id: 4,
		name: 'molla skele',
		phoneNumber: '09084432562',
		status: 'inactive',
		email: 'skele@gmail.com'
	},
	{
		id: 5,
		name: 'shade lateef',
		phoneNumber: '09084432562',
		status: 'active',
		email: 'shade@gmail.com'
	},
	{
		id: 6,
		name: 'idayat olateju',
		phoneNumber: '09084432562',
		status: 'inactive',
		email: 'olateju@gmail.com'
	},
	{
		id: 7,
		name: 'tony ricks',
		phoneNumber: '09084432562',
		status: 'active',
		email: 'tony@gmail.com'
	}

])

const deleteItems = (item) => {
	items.value.forEach((row, rowId) => {
		if(item == row){
			items.value.splice(rowId,1)
		}
	})
}
</script>