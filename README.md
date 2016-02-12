# Wordpress
- Заголовок сайта - <?php echo $blog_title = get_bloginfo( 'name' ); ?>  
- Описание сайта - <?php echo $blog_title = get_bloginfo( 'description' ); ?>  
- Заголовок рубрики - <?php echo get_cat_name(ID) ?>  
- Описание рубрики - <?php echo category_description( $category_id ); ?>
- 
<?php if ( have_posts() ) : query_posts('p=1');
while (have_posts()) : the_post(); ?>

<?php the_title(); ?>
<?php the_content(); ?>
<?php the_post_thumbnail(array(100, 100)); ?>

<? endwhile; endif; wp_reset_query(); ?>
