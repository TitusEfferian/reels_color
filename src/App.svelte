<script lang="ts">
	const color = [
		"bg-red-500",
		"bg-yellow-500",
		"bg-blue-500",
		"bg-purple-500",
		"bg-green-500",
		"bg-pink-500",
		"bg-black",
		"bg-white",
	];
	let width = 100;
	let height = 100;
	let borderRadius = 0;
	let count = 0;

	const handleOnclick = () => {
		width = Math.floor(Math.random() * 200) + 50;
		height = Math.floor(Math.random() * 200) + 50;
		borderRadius = (Math.floor(Math.random() * 200) + 50) / 2;
		count = count === color.length ? 0 : count + 1;
	};
</script>

<main class="flex items-center justify-center w-full h-screen">
	<div
		on:click={handleOnclick}
		style={`width: ${width}px; height:${height}px; border-radius:${borderRadius}px`}
		class={`${color[count]} transition-all`}
	/>
</main>
