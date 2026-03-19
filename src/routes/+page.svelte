<header>
	<div id="logo">
        <img src={title} alt="ZipShield" id="title"/>
        <img src={slogan} alt="Stop the snap." id="slogan" />
    </div>
</header>

<div id="problem">
    <p>Isn't it annoying when your zipper keeps flailing around, slapping you?</p>
    <p class="big_text">ZipShield is your solution.</p>
</div>

<div class="zs_pics">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
</div>

<p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p>


<script lang="ts">
    import title from "$lib/assets/title.png";
    import slogan from "$lib/assets/slogan.png";

    const placeholder_img = "https://media.istockphoto.com/id/1147544807/vector/thumbnail-image-vector-graphic.jpg?s=612x612&w=0&k=20&c=rnCKVbdxqkjlcs3xH87-9gocETqpspHFXu5dIGB4wuM=";
</script>



<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

    :root {
        color: white;

        font-family: "Poppins";
        font-size: 1.35rem;

        font-weight: bold;
    }

    :global(body) {
        background: linear-gradient(to bottom, #0b0b10, #161620);
        min-height: 100vh;
        margin: 0;
    }

    header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(15, 15, 25, .4);
            backdrop-filter: blur(8px) grayscale(30%);
            position: sticky;
            top: 0;
            z-index: 100;
    }

    #logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        margin: 0.8rem;
        margin-left: 2rem;

        img { animation: fadeIn 0.8s cubic-bezier(0.37, 0, 0.63, 1) both; }
        
        #title {
            width: 7rem;
        }

        #slogan {
            max-width: 85vw;
            width: 7rem;
            animation: fadeIn 0.8s cubic-bezier(0.37, 0, 0.63, 1) both;
        }
    }

    #problem {
        width: 100%;
        text-align: center;
    }

    .zs_pics {
        display: flex;
        align-items: center;
        justify-content: center;

        width: 100%;
        margin: auto;

        margin-bottom: 3rem;

        &:has(img:hover) img {
            transform: scale(0.85);
        }

        img:hover {
            transform: scale(1.2);
            box-shadow: 0 0 5px #00aaff, 0 0 40px #38bdff, 0 0 80px #89d8ff;
        }

        img {
            max-width: 20vw;
            max-height: 20vw;

            width: 20rem;
            height: 20rem;

            margin: auto;
            margin-top: 3rem;

            border: 7px solid #062339;

            transition: transform 0.3s cubic-bezier(0.37, 0, 0.63, 1),
                box-shadow 0.3s cubic-bezier(0.37, 0, 0.63, 1);

            &:hover {
                transform: scale(1.2) !important;
                box-shadow: 0 0 5px #00aaff, 0 0 40px #38bdff, 0 0 80px #89d8ff;
            }

            @supports (corner-shape: squircle) {
                border-radius: 40% / 40%;
                corner-shape: squircle;
            }

            @supports not (corner-shape: squircle) {
                border-radius: 20% / 20%;
            }
        }
    }
    /*#problem {
        //background-color: #00689c;
        background-color: #ffffff;
        color: #003d66;

        box-sizing: border-box;
        width: 100%;

        padding: 3rem;
        margin: auto;

        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    p {
        text-align: center;
        margin: 0.5rem;
        font-size: 1.35rem;
    }

    .big_text {
        font-size: 3rem;
        margin: 2rem;
    }

    #zs_pictures {
        display: flex;
        align-items: center;
        justify-content: center;

        width: 100%;
        margin: auto;

        margin-bottom: 3rem;

        &:has(img:hover) img {
            transform: scale(0.85);
        }

        img:hover {
            transform: scale(1.2);
            box-shadow: 0 0 5px #00aaff, 0 0 40px #38bdff, 0 0 80px #89d8ff;
        }

        img {
            max-width: 20vw;
            max-height: 20vw;

            width: 20rem;
            height: 20rem;

            margin: auto;
            margin-top: 3rem;

            border: 7px solid #062339;

            transition: transform 0.3s cubic-bezier(0.37, 0, 0.63, 1),
                box-shadow 0.3s cubic-bezier(0.37, 0, 0.63, 1);

            &:hover {
                transform: scale(1.2) !important;
                box-shadow: 0 0 5px #00aaff, 0 0 40px #38bdff, 0 0 80px #89d8ff;
            }

            @supports (corner-shape: squircle) {
                border-radius: 40% / 40%;
                corner-shape: squircle;
            }

            @supports not (corner-shape: squircle) {
                border-radius: 20% / 20%;
            }
        }
    }*/

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
