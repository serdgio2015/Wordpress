# Wordpress
- Подключение стилей - <?php bloginfo("template_directory"); ?>  
- Заголовок сайта - <?php bloginfo( 'name' ); ?>  
- Описание сайта - <?php bloginfo( 'description' ); ?>  
- Заголовок рубрики - <?php echo get_cat_name(ID) ?>  
- Описание рубрики - <?php echo category_description( $category_id ); ?>  
- Вывод цитаты - <?php the_excerpt(); ?>  
  <?php while ( have_posts() ) : the_post(); ?>   
  <?php endwhile; ?> 
- Если постов не нашлось пишем под постом:  
  <?php if ( have_posts()); ?> 
    <h3>Постов не нашлось</h3>
  <?php endif; ?> 

  <?php the_title(); ?>  
  <?php the_post(); ?>  
  <?php the_content(); ?>  
  <?php wp_nav_menu('primary'); ?>  
- Виджеты - <?php dynamic_sidebar(); ?>
  
  
  <?php the_post_thumbnail("thumbnail"); ?>  
  <?php the_post_thumbnail(array(100, 100)); ?>  

- Теги - <?php the_tags(); ?>  
- Рубрики - <?php the_category(); ?>  
- Время публикации поста - <?php the_time('d-m-Y'); ?> 
- Автор поста - <?php the_author(); ?>   

  <? endwhile; endif; wp_reset_query(); ?>
  
  - Переход на страницу записи. В ссылку заголовка записи вставляется - <?php the_permalink(); ?>
  
  
- Дополнительное поле - <?php echo get_post_meta($post->ID, 'year', true); ?>  
- Ссылка на большую картинку:  
  <?php   

  $large_image_url = wp_get_attachment_image_src( get_post_thumbnail_id(), 'large' );  
  echo $large_image_url[0]  

  ?>
- вывод комментариев в comments.php - <?php wp_list_comments(); ?>
- вывод комментариев на странице - <?php comments_template( 'comments.php' ); ?>

