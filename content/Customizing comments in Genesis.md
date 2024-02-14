---
draft: false
---

## Move comment form above comment list
```php
add_action( 'genesis_before_comments', 'wd_comment_checker' );
function wd_comment_checker() {
     if ( have_comments() ) { // only do this if the post has comments or it will remove the comment form
          remove_action( 'genesis_comment_form', 'genesis_do_comment_form' );
          add_action( 'genesis_list_comments', 'genesis_do_comment_form' , 5 );
     }
}
```

Via: [https://whiteleydesigns.com/code/move-comment-form-above-comment-list-in-genesis/](https://whiteleydesigns.com/code/move-comment-form-above-comment-list-in-genesis/)

## Change comment fields placeholder text
```php
//* Change comment form textarea to use placeholder
function ea_comment_textarea_placeholder( $args ) {
	$args['comment_field']        = str_replace( 'textarea', 'textarea placeholder="comment"', $args['comment_field'] );
	return $args;
}
add_filter( 'comment_form_defaults', 'ea_comment_textarea_placeholder' );
```

Via: [https://www.billerickson.net/code/use-placeholders-instead-of-labels-in-comment-form/](https://www.billerickson.net/code/use-placeholders-instead-of-labels-in-comment-form/)