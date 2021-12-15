<script>
    import Homecard from "./homecard.svelte"
    import Logo from "./Logo.svelte"

    const bands = [
        {
            name:"The Mountain Season",
            picture:"artistas/mountainseason.jpg",
            desc:``,
            links:[],
            date:"17/12 - 19h"
        },
        {
            name:"Razamanaz",
            picture:"",
            desc:``,
            links:[],
            date:"18/12 - 16h"
        },
        {
            name:"Cris DeLyra",
            picture:"artistas/crisdelyra.jpg",
            desc:``,
            links:[],
            date:"19/12 - 16h"
        },
        {
            name:"Flash",
            picture:"artistas/flash.jpg",
            desc:` `,
            links:[],
            date:"19/12 - 18h"
        },
        {
            name:"Andre Doninski",
            picture:"artistas/andre.jpg",
            desc:` `,
            links:[],
            date:"19/12 - 20h"
        },
        {
            name:" Loba & Nega Preto",
            picture:"",
            desc:` `,
            links:[],
            date:"19/12 - 22h"
        },
        {
            name:" Benedito",
            picture:"artistas/benedito.jpg",
            desc:` Benedito é músico, compositor e produtor musical, nascido em Minas Gerais, teve contato, ainda muito novo, com diversos estilos musicais. Tem como principais influências o Mpb e samba assim como o blues e jazz americanos. Junto com Álvaro Cardoso (bateria), Brenno Bronzi (baixo) e Yuri Castinheiras (guitarra), Benedito apresenta um projeto autoral onde procura expressar sua essência. `,
            links:[],
            date:"20/12 - 16h"
        },
        {
            name:" Fella",
            picture:"artistas/fella.jpg",
            desc:` Fella é um coletivo de rap idealizado na serra petropolitana do Rio de Janeiro 
pelos músicos e produtores Junior Ayres, Vinicius Junqueira e Arthur Ayres (Maipo Beats)
O Grupo conta com 3 artistas da região serrana: Aguiar, Crow e DJ NEW.`,
            links:[],
            date:"20/12 - 18h"
        },
        {
            name:" Jorge Amorim e Tribo",
            picture:"artistas/jorgeamorim.jpg",
            desc:` `,
            links:[],
            date:"20/12 - 20h"
        }
        ,
        {
            name:" ÀIYÉ",
            picture:"artistas/ayie.jpg",
            desc:`ÀIYÉ é como assina a baterista, cantora, compositora, produtora e artista sonora Larissa Conforto, que lançou em 2020 "Gratitrevas" pela Balaclava Records.

Gravado entre turnês e estradas do Brasil e Portugal, o álbum reúne espiritualidade, ritmos de resistência e experimentação eletrônica em um universo solitário e urgente, cujo show presencial já passou por Lisboa, Nova Iorque, e diversos estados brasileiros.`,
            links:[{name:"Youtube",href:"https://www.youtube.com/watch?v=KMc9PZxi3-g"}],
            date:"20/12 - 22h"
        }
        ,
        {
            name:"Hot Sofa",
            picture:"artistas/hotsofa.jpg",
            desc:`Hot Sofa surgiu especialmente para tocar no Solstício. A banda é formada por Luka Marques como principal compositor, vocalista e guitarrista base, Filipe Marques no baixo, Daniel   Quaresma na guitarra solo, Lucca Zapalla como baterista e também compositor e Pedro Goralski como tecladista e backing vocal. A banda tem como principais gêneros: MBP e rock alternativo. Luka, Filipe, Daniel e Pedro tocaram na edição do Solstício de Primavera 2021, Pedro com a banda Café Bordel e os 3 com a banda Clube da Montanha `,
            links:[],
            date:"21/12 - 16h"
        }
        ,
        {
            name:" Kika Notini",
            picture:"artistas/kika.jpg",
            desc:` `,
            links:[],
            date:"21/12 - 18h"
        }
        ,
        {
            name:" Dub Lyrio",
            picture:"artistas/dublyrio.jpg",
            desc:` Dub Lyrio é compositor, músico e dub master. Autor de centenas de composições tem um vasto repertório. 

Sua música envolve sincretismo, miscigenação e mistura. Bases eletrônicas mescladas entre dub, reggae, rock, hip hop entre outros estilos com letras cotidianas, espirituais e sempre a ótica única de um poeta trazem a autenticidade e originalidade de seu som e mensagem. `,
            links:[{name:"Spotify",href:"https://open.spotify.com/artist/5dr5vsvHp2e2Bt27HAMVNm?si=LgHyHTF4Qy6og-bWMyRGIg "},{name:"Instagram",href:"https://www.instagram.com/dublyrio "},{name:"Facebook",href:"https://www.facebook.com/dublyrio "}],
            date:"21/12 - 20h"
        },
        {
            name:" Palco Livre",
            picture:"",
            desc:`O Palco Livre é o momento de todos que quiserem participarem da Jam Session do Solstício de Verão. `,
            links:[],
            date:"21/12 - 20h"
        },
        // {
        //     name:" expo",
        //     picture:"",
        //     desc:` `,
        //     links:[],
        //     date:"21/12 - 20h"
        // }
        
    ]


</script>
<main>

    <h1 class="logo-holder">
        <Logo/>
    </h1>

    <article class="content">
        <h2>Solsti</h2>

        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rerum adipisci temporibus facere voluptatem cupiditate nesciunt alias, harum hic quaerat pariatur distinctio officia aliquam deleniti veritatis nulla ullam natus dignissimos accusamus.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rerum adipisci temporibus facere voluptatem cupiditate nesciunt alias, harum hic quaerat pariatur distinctio officia aliquam deleniti veritatis nulla ullam natus dignissimos accusamus.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rerum adipisci temporibus facere voluptatem cupiditate nesciunt alias, harum hic quaerat pariatur distinctio officia aliquam deleniti veritatis nulla ullam natus dignissimos accusamus.</p>

    </article>

    <article>

        <h2>Programação </h2>

        <div class="prog-grid">
            {#each bands as band}
                 <Homecard {...band}/>  
            {/each}
        </div>  
    </article>

</main>
<style>
    .logo-holder{
        max-height: calc(100vh - 90px);
        margin:auto;
        text-align: center;
    }
    main{
        max-width: 1100px;
        width:90vw;
        margin:auto;
        display: flex;
        justify-content: center;
        flex-direction: column;
        padding-bottom:90px
    }
    .content{
        text-align:center;
    }
    h2{
        text-align:center;
        font-size:60px;
    }
    @media (max-width:1100px){
        h2{
            font-size: 40px;
        }
    }

    @supports (-webkit-text-stroke-width: 2px) {
        h2{
            color:transparent;
            -webkit-text-stroke-width: 2px;
            -webkit-text-stroke-color: var(--white);
        }
    }
    /* .logo{
        max-width: 80px;
        width: 100%;
        margin:auto;
    } */

    .content{
        max-width:100%;
        font-size:20px;
    }
    @media (max-width:1100px){
        .content{
            font-size:17px;
        } 
    }

    .prog-grid{
        display:grid;
        grid-template-columns:1fr 1fr 1fr;
        grid-gap:20px;
        gap:20px;
        max-width: 990px;
        margin:auto;
    }

    @media (max-width:1100px){
        .prog-grid{
            grid-template-columns:1fr;
        }
    }
</style>