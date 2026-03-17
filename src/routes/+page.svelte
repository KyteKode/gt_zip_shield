<div id="logo">
    <img src={title} alt="ZipShield" id="title"/>
    <img src={slogan} alt="Stop the snap." id="slogan" />
</div>

<p>
    Isn't it a bit annoying when you're running
    and your zipper keeps flailing around, slapping you?
</p>

<p class="big_text">
    ZipShield has a solution for you!
</p>

<div>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
</div>



<script lang="ts">
    import title from "$lib/assets/title.png";
    import slogan from "$lib/assets/slogan.png";

    const placeholder_img = "https://developers.elementor.com/docs/assets/img/elementor-placeholder-image.png";
</script>



<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:ital,wght@0,100..700;1,100..700&display=swap');

    :root {
        background-color: #041826;
        color: #ffffff;

        font-family: "IBM Plex Sans", sans-serif;
        font-size: 1.35rem;

        font-weight: bold;
    }

    p {
        text-align: center;
        margin: 0.5rem;
    }

    .big_text {
        font-size: 2rem;
        margin: 1rem;
    }

    .zs_picture {
        max-width: 30vw;
        max-height: 30vw;

        width: 20rem;
        height: 20rem;

        margin: 2rem;

        @supports (corner-shape: squircle) {
            border-radius: 40% / 40%;
            corner-shape: squircle;
        }

        @supports not (corner-shape: squircle) {
            border-radius: 20% / 20%;
        }
    }

    #logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        margin: 1rem;
        margin-bottom: 2rem;

        img { animation: fadeIn 0.8s cubic-bezier(0.37, 0, 0.63, 1) both; }
        
        #title {
            max-width: 90vw;
            width: 20rem;
        }

        #slogan {
            max-width: 85vw;
            width: 18rem;
            animation: fadeIn 0.8s cubic-bezier(0.37, 0, 0.63, 1) both;
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
