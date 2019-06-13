<template>
  <div class="layout">
    <header>
        <div>
            <g-link to="/"><img src="images/Logo.svg"></g-link>
            
        </div>
        <nav>
            <ul>
                <li><g-link to="/">Home</g-link></li>
                <li><a href="/about">About</a></li>  
            </ul>
            <div class="img"><img src="images/Search.svg" alt=""></div>
        </nav>
    </header>
    <slot/>
    <footer>
       <div class="love"><span>Built by Samuel with</span><img src="images/path.svg" alt="love"></div>
    </footer>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
*{
    padding: 0;
    margin: 0;
    border: 0;
    text-decoration: none;
    list-style: none;
}

html, body{
    font-family: 'Roboto', sans-serif;
}

body{
    background-color: #F8F8F8;
   
}

.container{
    height: 100%;
    width: 90%;
    margin: auto;
}

h1, li a, span{
    font-family: 'Google Sans'
}

li a, span{
    color: #6A6A6A;
    font-size: 16px;
}

h1{
    font-size: 20px;
    font-weight: 600;
}

p{
    font-size: 15px;
    line-height: 1.6em;
}

h2{
    font-size: 16px;
    font-weight: 400;
    color: #5F64F5;
}

img{
    width: 90px;
}

.img img{
    display: block;
    width: 20px;
    margin: 0 0 0 50px ;

}

.love img{
    display: inline-block;
    width: 15px;
    margin-left: 5px;

}

/** Header **/

header{
    background: white;
    display: flex;
    justify-content: space-between;
    padding: 1em 60px; 
}

header nav{
    display: flex;
    margin-top: 5px;
}

header nav ul li{
    display: inline-block;
    margin-left: 40px
}

footer{
    background: white;
    align-items: center;
    text-align: center;
    padding: 1.6em;
}


</style>
