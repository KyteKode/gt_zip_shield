<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	import logo from "$lib/assets/logo.png";

	let { children } = $props();
</script>

<header>
	<a href="/">
		<img src={logo} alt="ZipShield" id="logo"/>
	</a>

	<!--<a href="/buy">Buy</a>-->
</header>

<svelte:head>
	<title>ZipShield</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<style lang="scss">
	:root {
        color: white;

        font-family: "Poppins";
        font-size: 1.35rem;

        font-weight: 400;
    }

    :global(body) {
        background: linear-gradient(to bottom, #0b0b10, #161620);
        min-height: 100vh;
        margin: 0;
    }

    header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(18, 18, 40, .7);
            backdrop-filter: blur(8px) grayscale(40%);
            position: sticky;
            top: 0;
            z-index: 100;

			padding: 0 2rem;
    }

	#logo {
        width: 9rem;

        margin-top: 0.8rem;
		margin-bottom: 0.4rem;
    }

	:global(.button) {
        transition: transform 0.3s cubic-bezier(0.37, 0, 0.63, 1),
            box-shadow 0.3s cubic-bezier(0.37, 0, 0.63, 1);

        background: #3b82f6;
        padding: 0.5rem 1rem;
        border-radius: 0.75rem;
        color: white;
        text-decoration: none;
        font-weight: 400;

        &:hover {
            box-shadow: 0 0 5px #00aaff, 0 0 20px #38bdff, 0 0 40px #89d8ff;
        }
    }

    a:not(:global(.button)) {
		transition: transform 0.3s cubic-bezier(0.37, 0, 0.63, 1),
        	color 0.3s cubic-bezier(0.37, 0, 0.63, 1);

		color: white;
        text-decoration: none;
		
		&:hover {
            color: #00aaff;
			transform: scale(1.2);
        }
	}

    :global(.bolded) {
        font-weight: 600;
    }

    :global(.row_wrapper) {
        display: flex;
        flex-direction: column;
        gap: 1rem;

        width: 100%;
        text-align: center;
    }
</style>

{@render children()}
