

<script>
    import Header from '$lib/Header.svelte'
    import Footer from '$lib/Footer.svelte'
</script>

<Header/>


<svelte:head><link rel="stylesheet" href="css/main.css" /></svelte:head>

<slot/>

<Footer/>