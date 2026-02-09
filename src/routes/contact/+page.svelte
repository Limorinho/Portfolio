<script lang="ts">
	let email = ""
	let subject = ""
	let message = ""
	let success = ""
	let error = ""
  
	async function submitForm() {
	  try {
		const res = await fetch('http://localhost:3000/contact', {
		  method: 'POST',
		  headers: { 'Content-Type': 'application/json' },
		  body: JSON.stringify({ email, subject, message })
		})
  
		if (res.ok) {
		  success = "Message sent!"
		  email = subject = message = ""
		} else {
		  throw new Error("Failed to send")
		}
	  } catch (e) {
		console.error(e)
		error = "Could not send message."
	  }
	}
  </script>

<h1 class="text-indigo-500 font-bold">Contact Us</h1>

<section class="max-w-xl mx-auto">
	<div class="py-8 lg:py-16">
		<p class="mx-auto text-center text-(--color-theme-1) md:text-lg">Got any questions or requests? go ahead and ask!</p>
		<form on:submit|preventDefault={submitForm} class="space-y-8 py-16">
			<div>
				<label for="email" class="block mb-2 font-bold">Your email</label>
				<input type="email" bind:value={email} id="email" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="name@email.com" required>
			</div>
			<div>
				<label for="subject" class="block mb-2 font-bold">Subject</label>
				<input type="text" bind:value={subject} required id="subject" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="Subject">
			</div>
			<div class="sm:col-span-2">
				<label for="message" class="block mb-2 font-bold">Your message</label>
				<textarea id="message" bind:value={message} required rows="6" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="add a message..."></textarea>
			</div>
			<div class="flex justify-center">
			  <button
					type="submit"
					class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Send message
					<svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" 
						xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
					<path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" 
							stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
					</svg>
		 	 </button>		  
			</div>
		</form>
		{#if success}<p>{success}</p>{/if}
		{#if error}<p class="text-red-500">{error}</p>{/if}
	</div>
  </section>

<style>
	form {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
	}
</style>
