<script>
    export let title = "Heading"
    export let subtitle = "Subtitle"
    import Image from "$lib/Image.svelte"
</script>

<header>
    <!--Heading text-->
    <div class="has-text-centered">
        <h1 class="title is-size-1">{title}</h1>
        <h2 class="subtitle is-size-2">{subtitle}</h2>
    </div>
</header>