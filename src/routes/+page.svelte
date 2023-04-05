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
<p>(malloc62 / Xodrium / Derv)</p>
</div>
        
<Section>
    <h2>Projects</h2>
    <div class='hwrap'>
        <Project name='PlanarCraph' url='https://planar.tdgmdev.net' img='https://planar.tdgmdev.net/favicon.svg' />
        <Project name='Sanifae' url='https://sanifae.tdgmdev.net/users/tdgmdev' img='https://sanifae.tdgmdev.net/icon_sanifae_black.svg' />
        <Project name='NeoScratchTree' url='https://tree.tdgmdev.net/?id=817940396' img='/img/favicon.svg' />
    </div>
    <h2>Contacts</h2>
    <div class='hwrap'>
        <Project name='GitHub' url='https://github.com/tdgmcode' img='/img/github-mark-white.svg' />
        <Project name='YouTube' url='https://www.youtube.com/channel/UCX9pYmio1T6yqS-ZjqyNnlg' img='https://www.youtube.com/favicon.ico' /> 
    </div>
    <h2>Extras</h2>
    <p>Matrix: <b>@derv:matrix.org</b></p>
    <p>Chat: <b>Xodrium#1333</b></p>
</Section>
