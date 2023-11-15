<template>
  <div class="wrapper">
    <Category v-for="i in Category" :key="i.Category"
   :bgcolor="i.bgcolor" 
            :image="i.image" 
            :Product="i.Product" 
            :quantity="i.quantity">

  </Category>
  </div>
  <br>

    <div class="promotion-container">
    <Promotion v-for=" i in Promotion" :key="i.Promotion"
    :colorBackground="i.colorBackground"
    :description="i.description"
    :productImages="i.productImages"
    :btnbgcolor="i.btnbgcolor"
    :btntext="i.btntext">
    </Promotion>
  </div>
  
  
</template>


<script>
import Category from "./components/category.vue";
import Button from "./components/button.vue";
import Promotion from "./components/promotion.vue";

export default{
  name: "App",
  components:{
    Category,
    Button,
    Promotion,
  },

  data(){
    return{
      Category: [
        {
          bgcolor: "#F2FCE4",
          image: "https://s3-alpha-sig.figma.com/img/8370/e915/8a586f746c0b10b70cd405c8aa1f2038?Expires=1701043200&Signature=nuVEq7Nzd19AIxIRLLEjSJVotSwf1Q0KQbNAiYbVgkNE3TOSq~ucJVycCTxCBYmbQQdUFEH5WfXShv-62DUKyiJPEpJD29tHB87AHvsFgxqc1iCXQ2L-10rCI~VY5yKs4GnpjD98VMyHdWy8aZo47gyn~IHBalBQRlRe5DUcvWVHazK98rv7d5gj3VyJgV7vjk6-8~EUVgXeP~chDa0uHx-PW7MZj3rr6~iZKQg9flxnR0FZ9w-CdzTmTf6YIn0i3UmwLbVzguHod5Oc-IYPVZ686Of4bNdPQQ6HEenKixqLqqLwAeF7MY4hsEpOzuL5Er2qhQBD2ysc79Qrw48x3Q__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Cake & Milk",
          quantity: "14 items"
        },
        {
          bgcolor: "#FFFCEB",
          image: "https://s3-alpha-sig.figma.com/img/fa19/6bce/6720167ebdfcf5d3f8a2d76053176f9a?Expires=1701043200&Signature=pJmjSAv83QimcuIG72nCNXlteOQAfTnga3FBqQAYSrQaYVGmTBOf6MZnPztVC6~7TSEazb1mNECezHkYjit02Y5mszQ5Gv6lfzgSiMmrllSqyhiZ6C9wx7P1DTJiltNv1lKqYD~z6jcnAQvcL7OxiLnLwKPozj1sSjXdEY8NV5nqy4nu03ZaOUh1DIZCXotAjC6Un0qr4mY8sQ5N1GnwUuZWipeHZ9mTWzXFYfWw2T3dG5RIjoE6uXREuWA4KYdDsMxYMANvr3fjNQp8yVQsllcJS47Det69Yw31CfmZ7TYCtVAOUTSx~A3VG9FM~Qdux4DUzPQwGv8d4wEEgYD4jw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Peach",
          quantity: "17 items"
        },
        {
          bgcolor: "#ECFFEC",
          image: "https://s3-alpha-sig.figma.com/img/eb0a/46d6/bf3d30616b8cd69f4b03064fe254350c?Expires=1700438400&Signature=aLIOwK3haNDGm28wEv~3ydG2WWISjMPCVXHwIP2uUGLGnVXF8Dpn5ukSByIbbdQOzXV8ztZjWYtesMl0NndF4IgTD4qzVmCnx9QWM0NbsH~38Y3jZfPRhCJDshpo5xAkHroJmHPMzW-FSTL~d1rUsZhHqY~8mRkq1gqc6frFx9B849bZJaJQtyCAdfsMmZJKLGIa3GqiF2lFOfbh6aSgnFEgjwwF6IuKaLaK4wRbpOPDWKgChw8sCOCkx4R0DPoKScrTHBSWcaWLTnysiIJbPvrhqx0vhENizxRxEi0WjbgHGfdopR6GiydgdrPyiaFB7kkljkuRjv2cU6UlEopaxA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Kiwi",
          quantity: "20 items",
        },
        {
          bgcolor: "#FEEFEA",
          image: "https://s3-alpha-sig.figma.com/img/21b6/3a1e/f2a493eea176934bcab372692ab59a29?Expires=1700438400&Signature=C8pXMKLGsoVh-QAb0YYrQJ24UhNr2fygtKuTTx4jPpt44cswZuIB0IR~7ejiXrW5dgk0z0wXbKxOcTPvgDE8PzqGtwdPpgzHBT17sedlsXMq2OjDgJBn2cpnHR6t3QXav~WO5aTDJfeW8kWVL-txXRjk4BrvghtdddWs1yMlcMvlFbXnAgetusMrpPJBnndGy30iC~PrpGrqdR5hlkOEZv9K-7t4lQYq1ZsvbTILUk1FjM2piVJubzOZfaR48P1F~DfCCKMZE8C-BtyTZNNR3yThMrI5ehKDoBQjy0b9qkYb2ZAnqS2tO1LAceMjMVjiU58uGQHRexPL-myspxyLcw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Apple",
          quantity: "10 items",
        },
        {
          bgcolor: "#FFF3EB",
          image: "https://s3-alpha-sig.figma.com/img/488c/b40d/98f6efd89c2347f8ab7f23b7757a7e2f?Expires=1700438400&Signature=dyIg6NMyCvlUdeyZNZgpbDwykM4epyRawh43jr05D6oGvT1ASk10HiJkbxxkzih2xRtouPhXCKLHdbU5GGhlTfBBVeNDolb6~lIMCSsTf5UzcPYJIfbmCsujzZ5pzJnpdCjf5JS-0jg9-Kfibl4krIcsR0Py7tz4xykwp9xqFYaQYODnYCbH1WnCn5sk5tgFwYLCqi61yVIEU~qHRkVPs28IePW5bu3jbhAG~j2SKw28l10lWF-7DT920N7rBjpFdpIyaOyddMiiqqxTOdo2HGLmUm3PosmGPMiACS02-lfxQAax87Pyroj-vdB-pdwgTDehom15aiFDXhXBOk2dyw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Snake",
          quantity: "15 items"
        },
        {
          bgcolor: "#FFF3FF",
          image: "https://s3-alpha-sig.figma.com/img/13f9/afc8/02816b515e817bcd88800c49b947f860?Expires=1701043200&Signature=S7xJJ2tNncqoFtfs0z49egQAhXp68WqXLqkKTd6iNqcX3dBe4VXW~0su0UwkKM5UuZzel51xlYQARTxfk6WGSm7Ny~CDaaMnClTd6oB917Wf~5-ALMdJjPQ2Xw~6cWxFZdtoEGMFGVSmK0CN~OeQviLSaiV2txUMPV7WaY9onC6M3NaAw1t7J231BGpJQoNeshOhAWuaOwm0X5TBmRHvMdthLe0UgdvjRS009zbvz-VKZ0k2ySDZ~4lu6qZt1KLpYm7blzbEFANdKwuzO5AiaEdoFz4CRQre0Dh46pzNcj18eiCeAbI8SDc6kR3qi7ocvE0bIGe4kQdRsiJgszQfQQ__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4", 
          Product: "Black plum",
          quantity: "25 items",
        },
        {
          bgcolor: "#F2FCE4",
          image: "https://s3-alpha-sig.figma.com/img/5e6d/35bc/cc6f73e5412576546dca6b013f4fc9c7?Expires=1701043200&Signature=jU~KGSCuxDZGaLS4p~Vhsve5DzsdY4MRm-GTsUC3hEAfHAy1xS-k9MYt15epdPytx4i1LVIFYGe9Bwbb-05S~UozKrJXPGNLO5kvn6Ci2O76VuDsYGXlT~YIbykAhMo26jzKZL-Wjh1T1gW36~g1t~nAFzW0cCjjwS62SOdo7JqqfcoA3Wl~G839qkElsj1OI~tzTQ8jHk4mXwyZVtBvu4PugxCZhyqP1vbmgCIS8IBesU8ZcB-P10L1FH-ydo-QKfxFn02nAALdg9DUDQcqa5ivHktuspJfVCRaZFF911cSVYEUmH5RH9dIzdWRggtT1pn~sCYCEqlTMyiDprJVtw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Vegetables",
          quantity: "65 items",
        },
        {
          bgcolor: "#FFFCEB",
          image: "https://s3-alpha-sig.figma.com/img/0ed9/44fa/3bcccc269ae2cadb2fb25ac9b02ea29e?Expires=1701043200&Signature=hrxIqePlHrVgOqGbOzXbpuZgoQl5KndljWGx5jMYf4gLll7Q~jR3fuRxAkwSRtkcComhPSR1UHNMurnw8fXV93jBJckQfXGBluo0A-dX9YEHEkmjtU6GSy~fc4m99cyUr82uaX2xoBW1h~qHFqHLEfH~fr12p471~VE5VO~oadkM6NbcFgHAkwPkjY~xLGvhjmSTJ03deKpSiwDEmV17TCntJvGfJrjg3LCQivogaZ8-CQQfyvpP5wwGScvRkQeeKMgQZ49wS8uYxd0X9l9hDO6NQhwjOQmq8uxHw4shPKfscaMxCMpRQin8r1RPKj-jC0eu4ipWU3gAG2uE1x2bDA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Headphone",
          quantity: "33 items",
        },
        {
          bgcolor: "#F2FCE4",
          image: "https://s3-alpha-sig.figma.com/img/78c4/8886/688817c7c490b88407c4904743141184?Expires=1701043200&Signature=ku2-TlVzwdx8vQkO5evcQ9lYiZ7pa25hkkW~W8Q4dUamLcd79akJ3MAiaKJm1L1dBk9pRr5bHMkaL2QyDLuBam5P~ww2zQTjKYF9vb8m1c~ZKqxx2XzcO-ivWYaUNN2dy6qm1hTnErhQWVOpvXZ3Cb5IH3~zraXFob1Sa4IQH8Tpq7UJ4V462dFFdByy4rfa8~ws34AzoKn9QTGWKlaYZYOaUqyqI7n9z843StdY7QyjF4v382hFdccYx8WeIdKAanH9Ii~gj2E-pnmbPUzmSrwLQp4mhomR3lNM0mh-emOmuFjzrBHNOOAvdBs-gltESpCUi4stDgQucLmtwkwQjg__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Cakes and milk",
          quantity: "54 items",
        },
        {
          bgcolor: "#FFF3FF",
          image: "https://s3-alpha-sig.figma.com/img/aadc/a20d/2ca905cbdfec3bf306fbe70e1ca34a8a?Expires=1701043200&Signature=JxcqdQZEapxcGc0zHoFUSJ2YOsHK6I1G2x54vW-7pk2K1FJWR27dJrRhoXt3Xt6fcpIXJsCVBX-kS-83PcZTJb-XNIIoZdxJzjml~HLHKcDtXpNrj2DQzfjFDaIQhrdOgSg~j7mYmiFgexGhJtc8jfFWCExCVN7ekRGMrVbr7zIcBDNuCx-WDyTfGOA8YxMJLwU4G~plPCReD2kyUiIuGfNu2EAIVdnz0rTqx175IbGJfEBJMVaCUSY-MJQpv1eqNfmGCkUKu8KWWuYdGUmjJW-azdxcUvIoiMjl~rO7328PmpATd4jsjZdUScn3XAsYbn6gWKHFIt1GA4LGcVkbBg__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          Product: "Oranges",
          quantity: "63 items",
        }

      ],
      Promotion: [
        {
          colorBackground: "#F0E8D5",
          productImages: "https://static7.depositphotos.com/1020804/753/i/450/depositphotos_7535602-stock-photo-onion-on-a-white-background.jpg",  
          description: "Everyday Fresh & Clean with Our Products",
          btnbgcolor: "#3BB77E",
          btntext: "Shop now",
        },
        {
          colorBackground: "#F3E8E8",
          productImages: "https://s3-alpha-sig.figma.com/img/2738/f29f/1c4542246febe8c91ddb74ce42b81c5d?Expires=1701043200&Signature=Vw-SeLTnk2PRQQzoW1xl3wEWmbg9rzrDbAC01ZXQL70KtE6Tl8o9hOXyqipKc0wDbJXeyz44tsXc7naEYe85qr3904zXkntmxby39sNRyXT8fYfLDa1rm7-0JjfICOGwchbSYGn2KrXI-LkfsVY7XH64YRWF1llOoq6l6xnwiQ6dxrCIQMgK9tfQtRZ8UZ1u639YoX8bVVPZ8iO3IwY8Ar5~wE3-2qyb1iBJdAnLv8Td6VFA3X4ZpMVG7dQaTk6e9V5N~rRuux-ypRe9~VR9AnmAa2PpnlkKQl4cCJ0ABuHFAjS-~7ASXuLGPUQe3f854~vIBBbHfKGXL5WA4gtcDg__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
          description: "Make your breakfast healthy and easy.",
          btnbgcolor: "#3BB77E",
          btntext: "Shop now",
        },
        {
          colorBackground:"#E7EAF3",
          productImages: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTda2STpcwnfA_ak-7UvKnhLiZ5rJKPfXmUEA&usqp=CAU",
          description: "The best organic product online",
          btnbgcolor: "#FDC040",
          btntext: "Shop now",
        }
      ],
    }
  },
}

</script>

<style scoped>
.promotion-container{
  display: flex;
  gap: 10px;
}
.wrapper{
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2px;
  gap: 32px;
}
</style>