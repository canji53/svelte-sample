<script lang="ts">
    import Footer from './Footer.svelte';
    import Header from './Header.svelte';
</script>

<div>
    <Header />
    <slot></slot>
    <Footer />
</div>