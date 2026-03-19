<div class="center_wrapper">
    <img src={slogan} alt="Stop the snap." id="slogan" />
    <p>Isn't it annoying when your zipper keeps flailing around, slapping you?</p>
    <p class="big_text">ZipShield is your solution.</p>
</div>

<div class="zs_pics">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
    <img src={placeholder_img} alt="Placeholder">
</div>

<div class="center_wrapper">
    <a class="button" href="/buy">Buy Now</a>
</div>

<p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p><p>Test</p>


<script lang="ts">
    import title from "$lib/assets/title.png";
    import slogan from "$lib/assets/slogan.png";

    const placeholder_img = "https://media.istockphoto.com/id/1147544807/vector/thumbnail-image-vector-graphic.jpg?s=612x612&w=0&k=20&c=rnCKVbdxqkjlcs3xH87-9gocETqpspHFXu5dIGB4wuM=";
</script>



<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

    .center_wrapper {
        width: 100%;
        text-align: center;

        margin-top: 2rem;
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
