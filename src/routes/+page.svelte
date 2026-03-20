<div id="hook">
    <img src={slogan} alt="Stop the snap." />
    <p>Isn't it annoying when your zipper keeps flailing around, slapping you?</p>
    <p class="big_text bolded">ZipShield is your solution.</p>
</div>

<div class="zs_pics">
    <div>
        <img src={placeholder_img} alt="Placeholder">
        <img src={placeholder_img} alt="Placeholder">
        <img src={placeholder_img} alt="Placeholder">
        <img src={placeholder_img} alt="Placeholder">
    </div>
</div>

<p id="desc">
    Zipshield slides onto your zipper and hangs onto the inside of your jacket to stop it from flailing.
    It is easy to make, being 3d printed with inexpensive PLA filament.
</p>

<div id="center_thingy">
    <p>You can buy this at:</p>
    <div id="buy_locations">
        <a class="button">Target</a>
        <a class="button">Walmart</a>
        <a class="button bolded" href="/buy">This website</a>
    </div>
</div>

<script lang="ts">
    import slogan from "$lib/assets/slogan.png";

    const placeholder_img = "https://media.istockphoto.com/id/1147544807/vector/thumbnail-image-vector-graphic.jpg?s=612x612&w=0&k=20&c=rnCKVbdxqkjlcs3xH87-9gocETqpspHFXu5dIGB4wuM=";
</script>



<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    
    #buy_locations {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: row;

        a { margin: 0 1rem; }
    }

    #center_thingy {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    #hook {
        width: 100%;
        text-align: center;

        img {
            width: 40rem;
            max-width: 90vw;
        }

        p {
            margin: 0.5rem;
        }
    }

    #desc {
        width: 100%;
        text-align: center;

        margin-top: 2rem;
    }

    .zs_pics {
        display: flex;
        align-items: center;
        justify-content: center;

        margin: 3rem;

        div {
            display: flex;
            align-items: center;
            justify-content: center;

            width: 90%;
        }

        &:has(img:hover) img {
            transform: scale(0.85);
        }

        img:hover {
            transform: scale(1.2);
            box-shadow: 0 0 5px #00aaff, 0 0 40px #38bdff, 0 0 80px #89d8ff;
        }

        img {
            max-width: 15vw;
            max-height: 15vw;

            width: 20rem;
            height: 20rem;

            margin: auto;

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
</style>
