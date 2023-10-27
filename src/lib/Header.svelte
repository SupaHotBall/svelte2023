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
            <div>
                <div class = "Gojo-gif">
                    <img src="../image/Gojo-running-gift.gif" alt="gojo">
                </div>
                <label for="active" on:click={hideMedia} class="glow-on-hover">Character</label>
            </div>    
            <label for="active" on:click={displayMedia} class="close">X</label>
            <div class="character-menu">
                <div>  
                <a href="/character1" on:click={e => { checked = !checked; }}>Gojo</a>
                <a href="/character2" on:click={e => { checked = !checked; }}>Ryomen</a>
                <a href="/character3" on:click={e => { checked = !checked; }}>Kento</a>
                </div>
            </div>           
        </div>

        <a href="/info">
            <button class="glow-on-hover" type="button">Info</button>
        </a>
            
        <a href="/about">
            <button class="glow-on-hover" type="button">About</button>
        </a>

    </div>

</header>

<div>
    
</div>