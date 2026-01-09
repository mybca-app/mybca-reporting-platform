<section class="mt-10 space-y-2 bg-slate-100 p-5">
	<h2 class="mb-5 font-serif text-2xl">Bus arrivals</h2>
	<p>
		This report provides a summary of all bus arrivals, as detected by myBCA's bus scanning service.
		The report is updated live. Data is sourced from BCA's bus spreadsheet.
	</p>
	<h3 class="mt-5 font-bold">Report columns</h3>
	<ul class="ml-5 list-disc">
		<li>
			<b>bus_name:</b>
			The name of the bus as it appears in the BCA bus spreadsheet.
		</li>
		<li>
			<b>bus_position:</b>
			The position that the bus parked in.
		</li>
		<li>
			<b>arrival_time:</b>
			The time at which the bus was <i>detected</i> by myBCA's systems. This time may be different
			from the time at which the bus actually
			<i>arrived</i>. Specifically, if the bus was one of the first buses to arrive on a given day,
			the arrival_time may be up to 5 minutes late and not represent the true arrival time of the
			bus. In other cases, the arrival_time can be up to 15 seconds late.
		</li>
	</ul>
	<div class="mt-5 space-y-2">
		<h3 class="font-bold">Generate report</h3>
		<p>Reports are provided as CSV files that can be opened in Excel or similar software.</p>
		<form action="https://main-service-prod-oc1.mybca.link/api/bus/reports/generate" method="GET">
			<div class="flex flex-col md:flex-row gap-3">
				<label for="bus-arrival-input-start" class="flex flex-col gap-1">
					Start date
					<input
						type="date"
						name="start"
						id="bus-arrival-input-start"
						value="2026-01-04"
						min="2026-01-04"
						class="border-slate-300 bg-slate-200"
					/>
				</label>
				<label for="bus-arrival-input-end" class="flex flex-col gap-1">
					End date
					<input
						type="date"
						name="end"
						id="bus-arrival-input-end"
						min="2026-01-04"
						class="border-slate-300 bg-slate-200"
					/>
				</label>
			</div>

			<div class="mt-8">
				<button type="submit" class="border border-accent-dark bg-accent hover:bg-accent-dark transition px-3 py-2 inline-flex gap-2 items-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="size-5"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3"
						/>
					</svg>

					Download report
				</button>
			</div>
		</form>
	</div>
</section>
