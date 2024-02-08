<script>
	import AboutTab from '$lib/components/business/AboutTab.svelte';
	import HoursTable from '$lib/components/business/HoursTable.svelte';
</script>

<div>
	<figure>
		<img
			class="w-full h-[30vh] object-cover rounded-lg"
			src="https://saharat-vithchataya.notion.site/images/page-cover/rijksmuseum_claesz_1628.jpg"
			alt="business_banner"
		/>
	</figure>
</div>
<div class="container mx-auto mb-28 px-3 md:px-32 lg:px-36">
	<section class="business-header mt-4">
		<div class="flex justify-between items-stretch">
			<div>
				<h1 class="text-white text-2xl font-semibold lg:text-3xl">Standardise Airport Hotel</h1>
				<div class=" text-sm font-medium mt-3">
					<button class="text-slate-300 btn btn-xs rounded-md cursor-default">Hotel</button>
					<span>·</span>
					<button
						class="btn btn-xs rounded-md"
						on:click={() => document.getElementById('my_modal_3').showModal()}
					>
						<span class="text-green-500">Opening</span>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 24 24"
							fill="currentColor"
							class="w-4 h-4"
						>
							<path
								fill-rule="evenodd"
								d="M2.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75S2.25 17.385 2.25 12Zm8.706-1.442c1.146-.573 2.437.463 2.126 1.706l-.709 2.836.042-.02a.75.75 0 0 1 .67 1.34l-.04.022c-1.147.573-2.438-.463-2.127-1.706l.71-2.836-.042.02a.75.75 0 1 1-.671-1.34l.041-.022ZM12 9a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Z"
								clip-rule="evenodd"
							/>
						</svg>
					</button>
					<dialog id="my_modal_3" class="modal">
						<div class="modal-box">
							<form method="dialog">
								<button class="btn btn-sm btn-circle btn-ghost absolute right-2 top-2">✕</button>
							</form>
							<HoursTable />
						</div>
					</dialog>

					<span>·</span>
					<button class="btn btn-xs rounded-md text-yellow-500 cursor-default">✨ 4.5</button>
				</div>
			</div>
		</div>
		<p class="mt-3 text-sm text-slate-300 md:text-sm">
			<!-- 🫠 -->
			Set 3 km from Airport International Airport, this relaxed hotel with a contemporary vibe is 4 km
			from Kalare Night Bazaar and 21 km from Doi Suthep Temple. The modern rooms feature Wi-Fi
		</p>
	</section>
	<!-- <div class="divider"></div> -->
	<div class="divider"></div>
	<section class="">
		<div role="tablist" class="tabs tabs-bordered bg-base-200 rounded-box w-full">
			<input type="radio" name="my_tabs_2" role="tab" class="tab" aria-label="Overviews" />
			<div role="tabpanel" class="tab-content bg-base-100 border-base-300 rounded-box p-6">
				Tab content 1
			</div>

			<input type="radio" name="my_tabs_2" role="tab" class="tab" aria-label="About" checked />
			<div role="tabpanel" class="tab-content bg-base-100 border-base-300 rounded-box p-3">
				<AboutTab />
			</div>

			<input type="radio" name="my_tabs_2" role="tab" class="tab" aria-label="Reviews" />
			<div role="tabpanel" class=" tab-content bg-base-100 border-base-300 rounded-box p-6">
				Tab content 3
			</div>
		</div>
	</section>
</div>
