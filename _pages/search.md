---
layout: page
title: Search.
---

<style>
	#search-container {
	    max-width: 100%;
	}
	input[type=text] {
	    padding: 0.9rem;
		background: none;
	    width: 100%;
		-webkit-appearance: none;
		font-family: inherit;
		font-size: 100%;
		border: .1rem solid #edf2f7;
        box-shadow: 0 .3rem 1.8rem rgba( 5, 10, 15, 0.07 );
        overflow: hidden;
	    outline: none;
	}
	#results-container {
		margin: .5rem 0;
        list-style-type: none;
	}
    #results-container li {
        margin-bottom: .2rem;
    }
    #results-container li a{
        text-decoration: none;
        color: #0066CC;
    }
    #results-container li a:hover{
        text-decoration: underline;
    }
</style>

<!-- Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" placeholder="Search ...">
<ul id="results-container"></ul>
</div>

<!-- Script pointing to search-script.js -->
<script src="/search.js" type="text/javascript"></script>

<!-- Configuration -->
<script type="text/javascript">
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  json: '/search.json',
  searchResultTemplate: '<li><a href="{url}" title="{desc}">{title}</a></li>',
  noResultsText: 'No results found',
  limit: 10,
  fuzzy: false,
  exclude: ['Welcome']
})
</script>