# Menu-de-Bootstrap-Para-Wordpress
Para Uso de Plantillas de Wordpress Con Bootstrap

Pasos para el menu en bootstrap
1.	Copiar en el tema el wp_bootstrap_navwalker.php que esta en esta carpeta.
2.	Se registra el .php en funtions.php // Registrar personalizada de navegación Walker

 require_once ( 'wp_bootstrap_navwalker.php'); // RESPONSIVE BOOSTRAP
3.	Se copia el siguiente codigo del menú


<nav class="navbar navbar-default">
  <div class="container-fluid padding-container">
    <!-- Brand and toggle get grouped for better mobile display -->
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
       <a class="navbar-brand" href="<?php echo home_url(); ?>">
						              <img src="<?php echo get_template_directory_uri(); ?>/img/logo-responsive.png" alt="Logo" class="logo-img">
						            </a>
    </div>

    <!-- Collect the nav links, forms, and other content for toggling -->
    <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
      <ul class="nav navbar-nav navbar-right">
           <?php
						            wp_nav_menu( array(
						                'menu'              => 'primary',
						                'theme_location'    => 'primary',
						                'depth'             => 2,
						                'container'         => 'div',
						                'container_class'   => 'collapse navbar-collapse',
						        		'container_id'      => 'bs-example-navbar-collapse-1',
						                'menu_class'        => 'nav navbar-nav navbar-right',
						                'fallback_cb'       => 'wp_bootstrap_navwalker::fallback',
						                'walker'            => new wp_bootstrap_navwalker())
						            );
						        ?>

      </ul>
     
  
    </div><!-- /.navbar-collapse -->
  </div><!-- /.container-fluid -->
</nav>
<!--navegador movil fin-->


Recordar que se debe registrar el css y js de bootstraps en el archivo de Funciones de Wordpress




Link de información:
http://stackoverflow.com/questions/25332527/convert-bootstrap-navbar-to-wordpress-menu
http://twittem.github.io/wp-bootstrap-navwalker/
http://blog.teamtreehouse.com/responsive-wordpress-bootstrap-theme-tutorial


