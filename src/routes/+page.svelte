<script>
    import Project from '$lib/Project.svelte';
    import Section from '$lib/Section.svelte';
</script>

<style>
    .fpage {
        flex-direction: row;
        align-items: space-around;
        justify-content: center;
        width: calc(100vw - 100px);

        padding: 50px;
        padding-top: 100px;
        padding-bottom: 150px;

        background: url(/img/border.svg) repeat-x 0% 100%/270px, var(--primary-1);
        color: var(--dark-3);

        overflow: hidden;
    
        display: flex;

        color: var(--light-1);
    }

    .fpage h3 {
        font-family: monospace;
    }

    .fpage img {
        height: 100px;
        animation: spin 5s linear infinite;
    }

    @keyframes spin { 100% { transform:rotate(360deg); } } 

    h3 {
        font-size: 3.7vmin;
        margin-bottom: 0;
    }

    h2 {
        text-align: center;
        width: 100%;
    }

    .fpage, .swrap, .hwrap {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .swrap {
        flex-direction: column;
        text-align: center;
        width: max(45vw, 500px);
    }

    .button {
        background: white;
        color: black;
        
        display: flex;
        width: fit-content;
        padding: 5px;
        border-radius: 10px;
        margin: 5px;
    }

    a {
        text-decoration: none;
    }
</style>

<div class='fpage'>
    <div class='swrap'>
        <img src='/img/favicon.svg'>
        <h3>tdgmcode</h3>
    </div>
    <div class='swrap'>
        <span>
            <p>I am a hobbyist developer primarily engineering web applications.</p>
            <div class='hwrap'>
                <div class='button'>♂️ He/Him</div>
                <div class='button'>📅 2008-03-28</div>
                <div class='button'>🖥️ Arch Linux</div>
                <div class='button'>✏️ SvelteKit</div>
                <div class='button'>✅ Self-Hosting</div>
            </div>
            <p><b>Main contacts</b></p>
            <p>Other accounts are for personal purposes, for advertising, or are being depecrated.</p>
            <div class='hwrap'>
                <div class='button'><a href='mailto:tdgmdev@gmail.com'>Email</a></div>
                <div class='button'><a href='https://github.com/tdgmcode'>GitHub</a></div>
                <div class='button'>Discord (tdgmcode#1333)</div>
                <div class='button'>Matrix (@derv:matrix.org)</div>
            </div>
        </span>
    </div>
</div>
        
<Section>
    <h2>Projects</h2>
    <div class='hwrap'>
        <Project name='Life Clock' url='/counter' img='/img/favicon.svg' >
            The amount of time until I turn 18.
        </Project>
        <Project name='Sanifae' url='https://sanifae.tdgmdev.net/users/tdgmdev' img='https://sanifae.tdgmdev.net/icon_sanifae_black.svg' >
            An experimental social network. Development on hold.
        </Project>
    </div>
</Section>
