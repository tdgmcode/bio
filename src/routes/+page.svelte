<script>
    import Project from '$lib/Project.svelte';
    import Section from '$lib/Section.svelte';
</script>

<style>
    .fpage {
        flex-direction: row;
        align-items: space-around;
        justify-content: center;
        width: 100vw;

        padding: 100px;
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
        width: max(50vw, 300px);
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
</style>

<div class='fpage'>
    <div class='swrap'>
        <img src='/img/favicon.svg'>
        <h3>tdgmcode</h3>
    </div>
    <div class='swrap'>
        <span>
            <p>I am a hobbyist developer. Some day, I strive to work professionally.</p>
            <div class='hwrap'>
                <div class='button'>♂️ he/him</div>
                <div class='button'>📅 2008-03-28</div>
                <div class='button'>🖥️ Arch Linux</div>
                <div class='button'>✏️ SvelteKit</div>
            </div>
            <p><b>My stances...</b></p>
            <div class='hwrap'>
                <div class='button'>✅ Self-Hosting</div>
                <div class='button'>✅ Open Source</div>
                <div class='button'>✅ Indie Development</div>
            </div>
            <div class='hwrap'>
                <div class='button'>❌ Website Builders</div>
                <div class='button'>❌ Big Tech</div>
                <div class='button'>❌ Windows</div>
                <div class='button'>❌ Internet Addicts</div>
                <div class='button'>❌ Petty Social Media Drama</div>
            </div>
        </span>
    </div>
</div>
        
<Section>
    <h2>Projects</h2>
    <div class='hwrap'>
        <Project name='Sanifae' url='https://sanifae.tdgmdev.net/users/tdgmdev' img='https://sanifae.tdgmdev.net/icon_sanifae_black.svg' />
    </div>
    <h2>Contacts</h2>
    <div class='hwrap'>
        <Project name='GitHub' url='https://github.com/tdgmcode' img='/img/github-mark-white.svg' />
        <Project name='Reddit' url='https://www.reddit.com/user/tdgmcode' img='https://www.reddit.com/favicon.ico' />
        <Project name='YouTube' url='https://www.youtube.com/@tdgmcode' img='https://www.youtube.com/favicon.ico' />
    </div>
    <h2>Extras</h2>
    <p>Matrix: <b>@derv:matrix.org</b></p>
    <p>Chat: <b>tdgmcode#1333</b></p>
</Section>
