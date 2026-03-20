<script lang=ts>
    let props = $props();
    let tasks = $derived(props.tasks)
    let date: Date = new Date()
    
</script>

{#each tasks as task, i} 
    {#if task.date < date}
        <div style="position: fixed; bottom: 0px; left: {(i%10)*10}vw; bottom: {Math.floor(i/10)*10}vw; width: 10vw; height: 10vw; padding: 5px; overflow: hidden; box-sizing: border-box">
            <div class="milk" style="background-size: cover; width: 100%; height: 100%; padding: 5px">
                <div class="thingy" style="font-size: 12px; width: 100%; height: 100%; overflow: hidden">
                    <span class="message">
                        PLEASE COMPLETE ME {task.submission}!!!! 
                    </span>
                </div>
            </div>
        </div>
    {/if}
{/each}