<script>
  import Logo from "./Logo.svelte"
</script>

<main>
    <div class="max-container">
        <a class="logo" href="/#/"><Logo/></a>
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
        border-bottom:2px solid #f8ab16;
        padding:10px;
        padding-bottom:0px;
    }
    .logo{
        display:block;
        height: auto;
        margin:auto;
        width: 100%;
        max-width: 84px;
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
@media (min-width:991px){	
nav a {
  font-size: 18px;
  font-weight: 500;
  }
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