#### Example ACF usage

```php
<?php while ( have_posts() ) : the_post(); ?>

  <?php the_field( 'hero_image' ); ?>
  <h1><?php the_title(); ?></h1>
  <?php the_content(); ?>

<?php endwhile; ?>
```