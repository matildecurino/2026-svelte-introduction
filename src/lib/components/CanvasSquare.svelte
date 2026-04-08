<script>
    let size = $state(50)
    let color = $state('#ff3e00')

    let canvas 

    $effect(() => { //onMount da usare solo una volta quando viene avviato. $effect fa rigirare il codice ogni volta che gli stati cambiano (size e color)
    const context = canvas.getContext("2d")
    context.clearRect(0,0, canvas.width, canvas.height)

    context.fillStyle = color 
    context.fillRect(0,0, size, size)
    })
</script>

<h3>Canvas Square</h3>

<article>
    <canvas bind:this={canvas} width="100" height="100"></canvas>

    <nav>
        <label>
            Size: <input type="range" bind:value={size}>
        </label>

        <label>
            Color: <input type="color" bind:value={color}>
        </label>

    </nav>
</article>

<p>{size} {color}</p>
<style>
    article {
        display : flex;
        gap: 1em;
        align-items: end;
    }

    canvas {
        border: solid 1px black;
    }

    nav {
        display: flex;
        gap: 1em;
        flex-direction: column;
    }

</style>