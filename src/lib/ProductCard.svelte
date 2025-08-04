<script>
  const productImgLrg = import.meta.env.BASE_URL + 'image-product-desktop.jpg';
  const productImgMob = import.meta.env.BASE_URL + 'image-product-mobile.jpg';
  import CartIcon from "./CartIcon.svelte";
</script>

<style>
  :root {
    --text-gray: hsl(228, 12%, 48%);
    --main-green-500: hsl(158, 36%, 37%);
    --main-green-700: hsl(158, 42%, 18%);
    --main-black: hsl(212, 21%, 14%);
    --main-grey: hsl(228, 12%, 48%);
    --main-cream: hsl(30, 38%, 92%);
    
    --font-xs: clamp(0.75rem, 1vw + 0.5rem, .75rem);
    --font-sm: clamp(0.875rem, 1.5vw + 0.5rem, 1rem);
    --font-base: clamp(1rem, 2vw + 0.5rem, 1.25rem);
    --font-lg: clamp(1.125rem, 2.5vw + 0.5rem, 1.5rem);
    --font-xl: clamp(1.25rem, 3.75vw + 0.5rem, 2rem);
    --font-2xl: clamp(1.5rem, 4vw + 0.5rem, 2.5rem);
    --font-3xl: clamp(1.875rem, 5vw + 0.5rem, 3rem);
    
    --font-xl-cust: clamp(1.25rem, 4vw + 0.5rem, 2rem);
    
    --lh-base: 1.5;
    --lh-tighter: 1.15;
    --lh-tight: 1;
  }
</style>


<!--
Desktop box is 600w x 450h
-->

<div
    class="grid sm:grid-cols-2 sm:grid-rows-6
           sm:max-w-[600px] sm:max-h-[450px] h-full w-full
           sm:aspect-[4/3] bg-white rounded-2xl
           sm:overflow-hidden border border-b-red-500"
>
  <div class="bg-gray-500 row-span-6 rounded-t-2xl md:rounded-t-none md:rounded-s-2xl overflow-hidden">
    <img src="{productImgLrg}" alt="Product Lg"
         class="object-cover object-[center_30%] sm:h-full sm:max-h-full w-full max-h-75">
  </div>
  <div class="bg-white row-span-6 text-left text-(--text-gray) flex flex-col justify-between p-8">
    <!--    TODO: Replicate weird spacing between each character -->
    <p class="font-extralight md:text-sm text-xs [letter-spacing:0.2rem] pb-4 sm:pb-0">PERFUME</p>
    <!--    TODO: On mobile, need to remove large space from line break think this has to do with line-height being unset from move away from TW -->
    <h2 class="font-['Fraunces'] text-(--main-black) [font-size:var(--font-xl-cust)] [line-height:var(--lh-tight)] font-bold pb-4 sm:pb-0">Gabrielle
      Essence Eau De Parfum</h2>
    <p class="md:text-sm text-xs [font-size:clamp(1rem, 0.8rem + 1vw, 3rem)] pb-4 sm:pb-0">A floral, solar and voluptuous
      interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.</p>
    <div class="flex items-center w-full pb-4 sm:pb-0">
      <span class="text-2xl font-['Fraunces'] text-[var(--main-green-500)]">$149.99</span>
      <span class="line-through text-xs font-['Montserrat'] text-[var(--text-gray)] ms-3">
    $169.99
  </span>
    </div>
    <button
        class="btn flex bg-(--main-green-500) hover:bg-(--main-green-700) text-white items-center justify-center text-xs font-semibold p-4">
      <CartIcon className="me-2"/>
      Add To Cart
    </button>
  </div>
</div>