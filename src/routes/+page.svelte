<div id="logo">
    <img src={title} alt="ZipShield" id="title"/>
    <img src={slogan} alt="Stop the snap." id="slogan" />
</div>

<div id="problem">
    <p>
        Isn't it annoying when you're running
       and your zipper keeps flailing around, slapping you?
    </p>
    <p class="big_text">
        ZipShield has a solution for you!
    </p>
</div>

<div id="zs_pictures">
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
    <img src={placeholder_img} alt="Placeholder" class="zs_picture"/>
</div>

<p>
    ZipShield solves this problem by attaching to the zipper's pull tab and the inside of your jacket.
    This product is 3d printed with PLA filament.
</p>



<script lang="ts">
    import title from "$lib/assets/title.png";
    import slogan from "$lib/assets/slogan.png";

    const placeholder_img = "https://media.istockphoto.com/id/1147544807/vector/thumbnail-image-vector-graphic.jpg?s=612x612&w=0&k=20&c=rnCKVbdxqkjlcs3xH87-9gocETqpspHFXu5dIGB4wuM=";
</script>



<style lang="scss">
    @import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:ital,wght@0,100..700;1,100..700&display=swap");

    :root {
        background: linear-gradient(30deg, #1474b9, #062338);
        //background-color: #093453;
        color: #ffffff;

        font-family: "IBM Plex Sans", sans-serif;
        font-size: 1.35rem;

        font-weight: bold;
        overflow-x: hidden;
    }

    #problem {
        //background-color: #00689c;
        background-color: #b3e1ff;
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
            max-width: 22.5vw;
            max-height: 22.5vw;

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
