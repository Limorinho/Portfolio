<script lang="ts">
</script>

<h1>Contact Us</h1>

<section class="">
	<div class="py-8 lg:py-16">
		<p class="mx-auto text-center text-(--color-theme-1) md:text-lg">Got a technical issue? Want to send feedback about a beta feature? Need details about our Business plan? Let us know.</p>
		<form action="#" class="space-y-8 py-16">
			<div>
				<label for="email" class="block mb-2 font-bold">Your email</label>
				<input type="email" id="email" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="name@email.com" required>
			</div>
			<div>
				<label for="subject" class="block mb-2 font-bold">Subject</label>
				<input type="text" id="subject" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="Let me know how I can help" required>
			</div>
			<div class="sm:col-span-2">
				<label for="message" class="block mb-2 font-bold">Your message</label>
				<textarea id="message" rows="6" class="bg-sky-500/30 text-sky-600 border-sky-500 block w-full text-sm bg-gray-50 rounded-lg shadow-sm border focus:ring-primary-500" placeholder="Leave a comment..."></textarea>
			</div>
			<button type="submit" class="py-3 text-center text-white rounded-lg bg-sky-700 sm:w-fit hover:bg-sky-800 focus:ring-4 focus:outline-none focus:ring-primary-300">Send message</button>
		</form>
	</div>
  </section>

<style>
	form {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
	}
	button {
		align-items: center;
	}
</style>
