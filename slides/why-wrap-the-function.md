### Why wrap the function?

<ul>
  <li class="fragment">Check that `get_field()` exists before calling it</li>
  <li class="fragment">Protect against empty data by defining a default value</li>
  <li class="fragment">Fail gracefully if ACF ever gets deactivated</li>
</ul>