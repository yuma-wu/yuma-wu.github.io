---
title: Blog
layout: default
permalink: "/blog/index.html"
---
<!-- Main -->
<section class="wrapper style1">
	<div class="container">
		<div id="content">
			<div class="row">
				<div class="12u">
					<!-- Blog -->
						<section>
<!-- 							
							<header class="major">
								<h2>The Blog</h2>
							</header>
-->
							{% assign blog_posts = site.posts | where: "type", "blog" %}
							{% for post in blog_posts limit: 4 %}
								<div class="row">
									<section class="12u">
										<div class="box post">
										<!-- 	{% if post.featured %}
												<a href="#" class="image left"><img src="{{ site.baseurl }}/assets/images{{ post.featured }}" alt=""></a>
											{% else %}
											    <a href="#" class="image left"><img src="{{ site.baseurl }}/assets/images/generic-blog-thumbnail.jpg" alt=""></a>
											{% endif %} -->
											<div class="inner">
												<h3>{{ post.title }} <small>({{ post.date | date: "%D" }})</small></h3> 
												{{ post.excerpt }}
												<footer>
													<a href="{{ site.baseurl }}{{ post.url }}" class="button">Continue Reading</a>
												</footer>
											</div>
										</div>
									</section>
								</div>
							{% endfor %}
							<h2>More posts:</h2>
							{% for post in blog_posts offset:4 %}
								<p>
									<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> <small>({{ post.date | date: "%D" }})</small>
								</p>
							{% endfor %}
						</section>
				</div>
			</div>
	</div>
</section>