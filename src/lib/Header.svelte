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
        
        <!-- Character tab with a checkbox to toggle visibility -->
        <div class="characters-tab">
            <!-- Checkbox input for toggling character menu visibility -->
            <input type="checkbox" id="active" {checked} on:change={e => { checked = !checked; }}>
            <!-- When you click the "Character" label, it shows the character menu. -->
            <label for="active" on:click={hideMedia} class="glow-on-hover">Character</label>
            <!-- when you click the "Character" label, it will close the menu -->
            <label for="active" on:click={displayMedia} class="close">X</label>

            <!-- Character menu links with js clicking -->
            <div class="character-menu">
                <div>
                    <!-- Links for different characters, clicking on them toggles the checkbox state -->
                <a href="/Gojo" on:click={e => { checked = !checked; }} class = "first-character">Gojo</a>
                <a href="/Ryomen" on:click={e => { checked = !checked; }} class = "second-character">Ryomen</a>
                <a href="/Kento" on:click={e => { checked = !checked; }} class = "third-character">Kento</a>
                </div>
            </div>           
        </div>

        <a href="/Slides">
            <button class="glow-on-hover" type="button">Photo Slider</button>
        </a>
            
        <a href="/About">
            <button class="glow-on-hover" type="button">About</button>
        </a>

    </div>

</header>