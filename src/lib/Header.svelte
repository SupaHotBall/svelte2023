<script>
    $:checked = false;
</script>

<header>
    
    <a class="logo-icon">JUJUTSU KAISEN</a>

    <div class="header-right">
        

        <a href="/">
            <button class="glow-on-hover" type="button">Home</button>
        </a>
        
        <div class="characters-tab">
            <input type="checkbox" id="active" {checked} on:change={e => { checked = !checked; }}>
            <label for="active" class="glow-on-hover">Character</label>
            <label for="active" class="close">X</label>
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