<script>
    export let name,picture,desc,links,date
    
</script>



    <div class="card">
        <div class="card___img">
            {#if picture}
                <img loading="lazy" src="{picture}" alt="{name}" >
            {:else}
                <img loading="lazy" src="artistas/solsticio.jpg" alt="{name}" >
            {/if}
        </div>
        <div class="card___content">
            <h3>{name}</h3>
            <div class="card___content___date">{date}</div>
            <div class="card___content___desc">{desc}</div>

            {#each links as link}
                <a class="sociallink" href="{link.href}">{link.name}</a>
            {/each}
        </div>
    </div>

    <style>
        .card{
            border-radius: 10px;
            -webkit-box-shadow: 0px 0px 9px 1px #0000000a;
            box-shadow: 0px 0px 9px 1px #0000000a;
            overflow:hidden;
            max-width:80vw;
            margin:auto;
            background: #ffffff1a;
            height: 100%;
        }
        img{
            background-color:#ff5d44;
            width:100%;
            max-width:340px;
        }
        
        .card___content{
            padding:10px;
        }

        .card___content___date{
            color:var(--yellow);
            font-weight: bold;
            font-size:16px;
            margin-bottom:10px;
        }

        h3{
            font-size:20px;
            margin-bottom:3px;
            margin-top: 0px;
        }

        .sociallink{
            background-color:var(--white);
            color:var(--orange);
            font-size:11px;
            padding:2px 10px;
            border-radius: 10px;
            display:inline-block;
            margin-top:20px;
            transition:all .3s;
            margin-right: 4px;
        }
        .sociallink:hover{
            text-decoration:none;
            background-color:var(--purple)
        }
        .card___content___desc{
            position: relative;
        }
        /* .card___content___desc:before{
            content:"";
            display:block;
            position:absolute;
            -webkit-box-shadow: inset 0px -49px 19px -14px rgba(0,0,0,0.8);
            box-shadow: inset 0px -49px 19px -14px hsl(8.2, 100%, 67.1%);
            width: 100%;
            height: 100%;
        } */
    </style>