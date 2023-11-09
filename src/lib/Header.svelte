<script>
    $:checked = false;

    const hideMedia = () => {
        const hide = document.querySelector(".span-items");
        hide.classList.add("hide");
    }

    const displayMedia = () =>{
        const display = document.querySelector(".span-items");
        display.classList.remove("hide");
    }

</script>

<header>
    
    <a href="/"><div class="Gojo-body-image" /></a>
    

    <div class="header-right">
        
        <div class="characters-tab">
            <input type="checkbox" id="active" {checked} on:change={e => { checked = !checked; }}>
            <label for="active" on:click={hideMedia} class="glow-on-hover">Character</label>
            <label for="active" on:click={displayMedia} class="close">X</label>
            <div class="character-menu">
                <div>
                <a href="/character1" on:click={e => { checked = !checked; }} class = "first-character">Gojo</a>
                <a href="/character2" on:click={e => { checked = !checked; }} class = "second-character">Ryomen</a>
                <a href="/character3" on:click={e => { checked = !checked; }} class = "third-character">Kento</a>
                </div>
            </div>           
        </div>

        <a href="/info">
            <button class="glow-on-hover" type="button">Photo Slider</button>
        </a>
            
        <a href="/About">
            <button class="glow-on-hover" type="button">About</button>
        </a>

    </div>

</header>