<script lang="ts">
	const links = [
		{
			title: 'Facebook',
			url: 'https://www.facebook.com/profile.php?id=100094335124661'
		},
		{
			title: 'Youtube',
			url: 'https://youtube.com'
		},
		{
			title: 'Instagram',
			url: 'https://instagram.com/standardise.group'
		}
	];
	const accessibility_and_anmenities = [
		{
			title: 'Service options',
			items: [
				{
					title: 'Outdoor seating',
					status: true
				},
				{
					title: 'Takeaway',
					status: true
				},
				{
					title: 'Dine-in',
					status: true
				}
			]
		},
		{
			title: 'Accessibility',
			items: [
				{
					title: 'Wheelchair-accessible car park',
					status: true
				},
				{
					title: 'Wheelchair-accessible entrance',
					status: true
				},
				{
					title: 'Wheelchair-accessible seating',
					status: true
				}
			]
		},
		{
			title: 'Offerings',
			items: [
				{
					title: 'Coffee',
					status: true
				},
				{
					title: 'Small plates',
					status: true
				}
			]
		},
		{
			title: 'Rules',
			items: [
				{
					title: 'Smoking',
					status: false
				}
			]
		}
	];
</script>

<div>
	<h2 class="text-xl font-medium">Details</h2>
	<div class="my-2 w-full h-auto rounded-lg border border-zinc-800 p-3">
		<section>
			<div class="divide-solid divide-zinc-800 divide-y-2">
				<div class="py-2">
					<div class="flex items-center gap-1">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="w-3 h-3 text-zinc-500"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
							/>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z"
							/>
						</svg>

						<h4 class="text-zinc-500 text-sm">Address</h4>
					</div>
					<a
						href="https://maps.app.goo.gl/2LyEp2nvmcwXUbh27"
						target="_blank"
						class="text-blue-600 text-sm"
					>
						Nong Chom, San Sai District, Chiang Mai 50210
					</a>
				</div>
				<div class="py-2">
					<div class="flex items-center gap-1">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="w-3 h-3 text-zinc-500"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z"
							/>
						</svg>
						<h4 class="text-zinc-500 text-sm">Phone</h4>
					</div>
					<a href="tel:0983631425" class="text-sm text-blue-600">+66 65-310-6914</a>
				</div>
				<div class="py-2">
					<div class="flex items-center gap-x-1">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="w-3 h-3 text-zinc-500"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M13.19 8.688a4.5 4.5 0 0 1 1.242 7.244l-4.5 4.5a4.5 4.5 0 0 1-6.364-6.364l1.757-1.757m13.35-.622 1.757-1.757a4.5 4.5 0 0 0-6.364-6.364l-4.5 4.5a4.5 4.5 0 0 0 1.242 7.244"
							/>
						</svg>
						<h4 class="text-zinc-500 text-sm">Links</h4>
					</div>
					<ul class=" text-blue-600 text-sm">
						<li class="">
							{#each links as link}
								<li>
									<a href={link.url} target="_blank">{link.title}</a>
								</li>
							{/each}
						</li>
					</ul>
				</div>
			</div>
		</section>
	</div>
	<h2 class="text-xl font-medium">Accessibility and Aamenities</h2>
	<div class="my-2 w-full h-auto rounded-lg border border-zinc-800 p-3">
		<div class="divide-solid divide-zinc-800 divide-y-2">
			{#each accessibility_and_anmenities as item}
				<section class="py-2">
					<h4 class="font-bold">{item.title}</h4>
					{#each item.items as value}
						<div class="flex items-center gap-1 mt-1">
							{#if value.status}
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="w-4 h-4 text-green-500"
								>
									<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
								</svg>
							{:else}
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="w-4 h-4 text-red-500"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M18.364 18.364A9 9 0 0 0 5.636 5.636m12.728 12.728A9 9 0 0 1 5.636 5.636m12.728 12.728L5.636 5.636"
									/>
								</svg>
							{/if}

							<span class="text-sm pr-3">{value.title}</span>
						</div>
					{/each}
				</section>
			{/each}
		</div>
	</div>
</div>
