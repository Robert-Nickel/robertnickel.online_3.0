<script>
    import { browser } from "$app/environment";
    if (browser) {
        import("@whereby.com/browser-sdk/embed");
    }
</script>
<div class="whereby-container">
    <whereby-embed
        room="https://robertnickel.whereby.com/coachingc8e005b9-46c7-46d3-b269-e47771f8d2bf"
    ></whereby-embed>
</div>

<style>
    .whereby-container {
        height: 100vh;
        overflow: hidden;
    }

    whereby-embed {
        width: 100%;
        height: 100%;
    }
</style>
