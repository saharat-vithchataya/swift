<script>
	import BottomNavigatoin from '$lib/components/BottomNavigatoin.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import '../app.css';
</script>

<Navbar />
<slot />
<BottomNavigatoin />
