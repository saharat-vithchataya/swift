<script>
	const hours_data = [
		{
			day: 'Monday',
			hours: '9:10AM-6:30PM'
		},
		{
			day: 'Tuesday',
			hours: '9:10AM-6:30PM'
		},
		{
			day: 'Wednesday',
			hours: '9:10AM-6:30PM'
		},
		{
			day: 'Thursday',
			hours: '9:10AM-6:30PM'
		},
		{
			day: 'Saturday',
			hours: 'Open 24 Hours'
		},
		{
			day: 'Sunday',
			hours: null
		}
	];
</script>

<!-- You can open the modal using ID.showModal() method -->
<div class="overflow-x-auto">
	<h3 class="text-lg">Hours table</h3>
	<table class="table">
		<!-- head -->
		<thead>
			<tr>
				<th></th>
				<th></th>
			</tr>
		</thead>
		<tbody>
			<!-- row 1 -->
			{#each hours_data as item}
				<tr class="hover">
					<td class="text-xs lg:text-sm font-semibold">{item.day}</td>
					<td class="text-xs lg:text-sm font-normal">
						{#if item.hours == null}
							<span class="text-red-500">Closed</span>
						{:else}
							{item.hours}
						{/if}
					</td>
				</tr>
			{/each}
		</tbody>
	</table>
</div>
