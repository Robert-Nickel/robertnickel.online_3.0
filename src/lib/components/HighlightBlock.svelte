<script lang="ts">
    import { onMount } from "svelte";

    export let mobileAutoActive = true;
    export let activeColor = "#ffff00";
    export let shiftX = 16;

    let element: HTMLDivElement;
    let isActive = false;
    let isTouchViewport = false;

    function updateViewportMode() {
        isTouchViewport = window.matchMedia(
            "(hover: none), (pointer: coarse)",
        ).matches;
    }

    function updateActiveByViewportCenter() {
        if (!mobileAutoActive || !isTouchViewport || !element) {
            isActive = false;
            return;
        }

        const rect = element.getBoundingClientRect();
        const elementCenter = rect.top + rect.height / 2;
        const viewportCenter = window.innerHeight / 2;

        const threshold = Math.min(140, rect.height / 2 + 40);
        isActive = Math.abs(elementCenter - viewportCenter) < threshold;
    }

    onMount(() => {
        updateViewportMode();
        updateActiveByViewportCenter();

        const mediaQuery = window.matchMedia(
            "(hover: none), (pointer: coarse)",
        );

        const handleChange = () => {
            updateViewportMode();
            updateActiveByViewportCenter();
        };

        const handleScroll = () => {
            updateActiveByViewportCenter();
        };

        const handleResize = () => {
            updateViewportMode();
            updateActiveByViewportCenter();
        };

        mediaQuery.addEventListener("change", handleChange);
        window.addEventListener("scroll", handleScroll, { passive: true });
        window.addEventListener("resize", handleResize);

        return () => {
            mediaQuery.removeEventListener("change", handleChange);
            window.removeEventListener("scroll", handleScroll);
            window.removeEventListener("resize", handleResize);
        };
    });
</script>

<div
    bind:this={element}
    class="highlight-block"
    class:active={isActive}
    style={`--highlight-color: ${activeColor}; --shift-x: ${shiftX}px;`}
>
    <div class="highlight-content">
        <slot />
    </div>
</div>

<style>
    .highlight-block {
        position: relative;
    }

    .highlight-content {
        padding-left: 0;
        transition: transform 180ms ease;
    }

    .highlight-block::before {
        content: "";
        position: absolute;
        left: 0;
        top: 0;
        width: 6px;
        height: 100%;
        background: var(--highlight-color);

        opacity: 0;
        transform: scaleX(0);
        transform-origin: left;

        transition:
            opacity 120ms ease,
            transform 200ms ease;
    }

    /* Desktop (Hover) */
    @media (hover: hover) and (pointer: fine) {
        .highlight-block:hover .highlight-content {
            transform: translateX(var(--shift-x));
        }

        .highlight-block:hover::before {
            opacity: 1;
            transform: scaleX(1);
        }
    }

    /* Mobile (Scroll aktiv) */
    .highlight-block.active .highlight-content {
        transform: translateX(var(--shift-x));
    }

    .highlight-block.active::before {
        opacity: 1;
        transform: scaleX(1);
    }
</style>
