<script>
  import { onMount } from 'svelte';
  
  export let delay = 0;
  export let duration = 600;
  
  let element;
  let isVisible = false;
  
  onMount(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting && !isVisible) {
            isVisible = true;
          }
        });
      },
      {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
      }
    );
    
    if (element) {
      observer.observe(element);
    }
    
    return () => {
      if (element) {
        observer.unobserve(element);
      }
    };
  });
</script>

<div 
  bind:this={element}
  class="fade-in-up"
  class:visible={isVisible}
  style="--delay: {delay}ms; --duration: {duration}ms;"
>
  <slot />
</div>

<style>
  .fade-in-up {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity var(--duration) ease-out var(--delay), 
                transform var(--duration) ease-out var(--delay);
  }
  
  .fade-in-up.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
