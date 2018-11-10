<template>
  <div class="padre">
    <header class="header"><!--esto es el header lo que corresponde a todo lo negro que se observa-->
      <div class="menu"><!--Este corresponde al menu-->
        <div class="logo">
          <!--<img src="./imagenes/logo.png">-->
          <a>Clinic Cen</a>
        </div>
        <nav class="nav">
          <a><i class="fa fa-home" aria-hidden="true"></i>Inicio</a>
          <a><i class="fa fa-user" aria-hidden="true"></i>Nosotros</a>
          <a><i class="fa fa-comments" aria-hidden="true"></i>Servicios</a>
          <a><i class="fa fa-book-reader" aria-hidden="true"></i>Noticias</a>
          <a><i class="fa fa-envelope" aria-hidden="true"></i>Contacto</a>
        </nav>
        <div class="social">
          <div><a><i class="fab fa-facebook-square" aria-hidden="true"></i></a></div>
          <div><a><i class="fab fa-twitter-square" aria-hidden="true"></i></a></div>
        </div>
      </div>
    </header>
    <section>
      <div class="slider">
        <ul>
          <li><img src="./imagenes/salud.jpg"></li>
          <li><img src="./imagenes/instalaciones.jpg"></li>
          <li><img src="./imagenes/cirugia.jpg"></li>
          <li><img src="./imagenes/tecnologia.jpg"></li>
        </ul>
      </div>
    </section>
    <section class="section"><!--Esta es la otra parte seccion-->
      <div class="articulos">
        <article-box/>
        <article-box/>
        <article-box/>
        <article-box/>
      </div>
      <nav class="navegacion"></nav>
      <aside class="aside"> <!--corresponde a la caja verde de la parte derecha-->
        <div class="publicidad"></div>
        <div class="publicidad"></div>
      </aside>
    </section>
    <footer class="footer"><!--Esto corresponde a la ultima caja-->
      <nav class="pie"></nav>
    </footer>
  </div>
</template>

<script>
import ArticleBox from './components/ArticleBox.vue'
export default {
  components: { ArticleBox }
}
</script>

<style>
@import "./estilos/base.scss";
</style>

<style>
*{  /*estilos generales */
  margin:0px;
  padding:7px;
  box-sizing:border-box; /*Esto es para que las cajas no se fusionen unas con otras */
}
template{
  font-family:'Montserrat',sans-serif;
}
.padre{
  display:flex;
  flex-flow:column nowrap;  /* se va a poner en columnas  y no wrap se va a adaptar al tamaño deseado volviendo a verse como estaba antes*/
}
  .header{
    display:flex;
    flex-flow:column nowrap;/*Para que quede en columnas y se adpate al tamaño que se quiere*/
  }
    .menu{
      background:#70a3c4;
      opacity:.8;
      display:flex;
      flex-flow:row nowrap; /*row para que se muester en columnas y nowrap para que se muestra en la misma linea*/
      height:100px; /*una altura mas grande*/
      align-items:center; /*esto es para centrar los items*/
    }
      .logo{ /*Este al principio se ve uno debajo del otro*/
        flex:1 1 auto; /*esto es para que ocupe el 100% del contendor*/
        /*color:#fff este color no aplica ya que esto no se esta incorporando del todo al ancla o a la etiqueta a */
      }
        .logo a{
          color:#fff;
          font-size:30px;
        }
        .logo a:hover{
          color:#343434;
        }
       /* .logo img{
          width:88px;
          height:auto;
        }*/
      .nav{
        flex:5 1 auto; /*Con esto va a ser 5 veces el tamaño de los demas contenedores*/
      }
        .nav a{
          color:#fff;
          font-size: 11px;
          text-transform: uppercase;
          padding: 0 10px;
          letter-spacing: 2px; /*Esto es para que se separen las letras en dos pixeles cada una*/
        }
        .nav a:hover{
          color:#343434;
        }
      .social{
        flex:1 1 auto;
        display:flex; /*para que los iconos queden uno enseguida del otro*/
      }
        .social a{
          font-size:18px;
          color:#fff;
          padding: 0 5px; /*0 hacia arriba y hacia abajo y uno hacia los lados*/
        }
        .social a:hover{
          color:#343434;
        }
  .slider{
    background: #f07b3f;
    margin:auto;
    overflow:hidden; /*Para que los elementos que estan por fuera no se vean*/
  }
    .slider ul{
      padding:0;
      display:flex;
      width:400%;
      border:none;
    }
    .slider li{
      list-style:none;
      margin:0;
      padding:0;
    }
    .slider img{
      width:100%;
    }
  .section{
    background:#000;
    display:flex;
  }
    .articulos{
      background:#4e4e6a;
      flex: 2 1 auto;
      display:flex;/*para que los articulos esten uno enseguida del otro*/
      flex-flow:row wrap;
    }
      .article{
        background:#1f6cb0;
        flex:1 1 40%;
      }
        .article img{
          width:300px;
          height:300px;
        }
      .navegacion{
        background:#70a3c4;
        flex:1 1 100%;
      }
    .aside{
      background:#f73f52;
      flex:1 1 auto;
    }
      .publicidad{
        background:#ffea85;
      }
  .footer{
    background:#000;
    display:flex;
    justify-content: center; /*esto es para centrar el item ya que esto va a centrar todos los contenedores hijos*/
  }
    .pie{
      background:#e6af2e;
      width:300px; /*Con esto se posiciona al lado izquierdo*/
    }

@media all and (max-width: 414px){ /* con esto querio decir que de  0 a 800 me aplique los siguientes estilos*/
  .section{
    flex-direction: column;
  }
  .menu{
    flex-direction:column;  /*columna es para que se vea uno debajo del otro*/
    height: auto;/*con esto se le dice que el alto sea de forma automatica*/
  }
  .aside{  /*Con esto quiero uno del lado del otro*/
    display:flex;
    justify-content:center;
  }
}
@media all and (max-width: 360px){ /*de este tamaño se vea uno debajo de la otra*/
  .aside{
    flex-direction:column;
  }
}
</style>

<!--Sitio web colorhunt.co/c/7247-->
<!--Es importante solo dar altura al contenedor-->
