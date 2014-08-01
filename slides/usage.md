###### Usage

```php
<?php
  $fields = array( 'image', 'headline', 'link' );
  $slides = themename_get_repeater_content( 'hero_carousel', null, $slides );
  if ( $slides ) :
?>

  <div id="hero-carousel">
    <?php foreach ( $slides as $slide ) : ?>

      <div>
        <a href="<?php echo $slide['link']; ?>">
          <?php echo wp_get_attachment_image( $slide['image'], 'large' ); ?>
          <?php echo $slide['headline']; ?>
        </a>
      </div>

    <?php endforeach; ?>
  </div>

<?php endif; ?>
```