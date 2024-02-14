---
draft: false
---
Creates a shortcode that can be inserted into Beaver Builder that displays the search count and term.

```php
//* Display search results count and term via shortcode
function ab_get_search_count() {
	global $wp_query;
	$search_query = get_search_query();
	$not_singular = $wp_query->found_posts > 1 ? 'results for:' : 'result for:'; 
	return $wp_query->found_posts . " $not_singular " . $search_query;
}
add_shortcode('searchcount', 'ab_get_search_count');
```

Using the following shortcode:

```shortcode
[searchcount]
```

The output is:
```output
# result(s) for: XYZ
```

