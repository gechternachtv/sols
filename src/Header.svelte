<main>
    <div class="max-container">
        <a href="/#/"><img src="/assets/logo_completa02.jpg" alt=""></a>
        <nav>
            <a href="/#/">Programação</a>
            <a href="/#/Convite">Convite</a>
        </nav>
    </div>
</main>
<style>
main{
    background-color:var(--orange);
    margin-top:0px;
}

    .max-container{
        margin:auto;
        max-width:1140px;
        display: flex;
        border-bottom:2px solid var(--white);
        padding:10px;
    }
    img{
        display:block;
        height: auto;
        max-width: 50px;
        margin:auto
    }





nav {
  max-width: 800px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
}

nav a {
  flex-grow: 1;
  text-align: center;
  padding: 1em;
  position: relative;
}

nav a:hover {
    text-decoration: none;
    font-style: none;;
}
nav a::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 2px;
  transform: scaleX(0);
  background: var(--white);
  transition: 0.7s transform cubic-bezier(0.06, 0.9, 0.28, 1);
}

nav a:hover::after {
  transform: scaleX(1);
}
</style>