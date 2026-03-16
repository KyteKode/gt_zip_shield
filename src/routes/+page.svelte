<div id="logo">
    <img src={title} alt="ZipShield" id="title"/>
    <img src={slogan} alt="Stop the snap." id="slogan" />
</div>

<p>
    Isn't it a bit annoying when you're running
    and your zipper keeps flailing around, slapping you?
</p>



<script lang="ts">
    import title from "$lib/assets/title.png";
    import slogan from "$lib/assets/slogan.png";
</script>



<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:ital,wght@0,100..700;1,100..700&display=swap');

    :global(body) {
        background-color: #041826;
        color: #ffffff;

        font-family: "IBM Plex Sans", sans-serif;
        font-size: 4vh;
    }

    #logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        
        #title {
            max-height: 20vh;
            animation: fadeIn 0.8s cubic-bezier(0.37, 0, 0.63, 1) both;
        }

        #slogan {
            max-height: 7vh;
            animation: fadeIn 1.0s cubic-bezier(0.37, 0, 0.63, 1) both;
        }
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: scale(0.2);
        }
        to {
            opacity: 1;
            transform: scale(1);
        }
    }
</style>
