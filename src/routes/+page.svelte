<script>
    import Project from '$lib/Project.svelte';
    import Section from '$lib/Section.svelte';
</script>

<style>
    .fpage {
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100vw;
        height: 350px;
        margin-bottom: 100px;

        background: url(/img/border.svg) repeat-x 0% 100%/270px, var(--primary-1);
        color: var(--dark-3);

        overflow: hidden;
    
        display: flex;

        color: var(--light-1);

        animation: translate 3s ease-in-out infinite;
    }

    .fpage h3 {
        filter: drop-shadow(0 0 8px rgba(255,255,255,1));
        font-family: monospace;
    }

    .fpage img {
        height: 100px;
        animation: spin 5s linear infinite;
    }

    @keyframes spin { 100% { transform:rotate(360deg); } } 

    @keyframes translate { 
        50% { 
            background: url(/img/border.svg) repeat-x 700px 100%/150px, var(--primary-1); 
            height: 450px; 
            margin-bottom: 0;
        } 

        80% { 
            background: url(/img/border.svg) repeat-x 0% 100%/400px, var(--primary-1);
        } 
    }

    h3 {
        font-size: 3.7vmin;
        margin-bottom: 0;
    }

    h2 {
        text-align: center;
        width: 100%;
    }

    .hwrap {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>

<div class='fpage'>
<img src='/img/favicon.svg'>
<h3>tdgmcode</h3>
</div>
        
<Section>
    <h2>Projects</h2>
    <div class='hwrap'>
        <Project name='Sanifae' url='https://sanifae.tdgmdev.net/users/tdgmdev' img='https://sanifae.tdgmdev.net/icon_sanifae_black.svg' />
    </div>
    <h2>Contacts</h2>
    <div class='hwrap'>
        <Project name='GitHub' url='https://github.com/tdgmcode' img='/img/github-mark-white.svg' />
        <Project name='Sketchers United' url='https://sketchersunited.org/users/208210' img='https://sketchersunited.org/pwa/favicon-32x32.png' />
        <Project name='YouTube' url='https://www.youtube.com/channel/UC8XuOpsm85rVTMcT2Tb7d8w' img='https://www.youtube.com/favicon.ico' /> 
        <Project name='Twitter' url='https://twitter.com/char__pointer' img='https://abs.twimg.com/favicons/twitter.2.ico' />
        <Project name='Reddit' url='https://www.reddit.com/user/tdgmcode' img='https://www.reddit.com/favicon.ico' />
        <Project name='DeviantArt' url='https://www.deviantart.com/malloc62' img='https://st.deviantart.net/eclipse/icons/favicon-v2-32x32.png' />
        <Project name='Condensed' url='https://condensed.lunarsphere.net/u/tdgmcode/' img='https://condensed.lunarsphere.net/img/branding/icon.svg' />
    </div>
    <h2>Extras</h2>
    <p>Matrix: <b>@derv:matrix.org</b></p>
    <p>Chat: <b>tdgmcode#1333</b></p>
</Section>
