<strong>Haha</strong>

    {% for post in paginator.posts %}

    <article class="post">
        <header class="post-header">
            <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        </header>
        <section class="post-excerpt">
            {{ post.excerpt }} <a class="read-more" href="{{ post.url | relative_url }}">&raquo;</a>
        </section>
        <footer class="post-meta">
            {% if site.author %}
                <img class="author-thumb" src="{{'/assets/images/profile.png' | prepend: site.baseurl_root }}" alt="Author's profile picture" nopin="nopin" />
                {{ site.author }}
            {% endif %}
            {% if post.categories.size > 0 %} 
                {{ post.categories | array_to_sentence_string | prepend: 'on ' }} 
            {% endif %}
            <time class="post-date" datetime="{{ post.date | date:"%Y-%m-%d" }}">
                {{ post.date | date_to_string }}
            </time> 
        </footer>
    </article>

    {% endfor %}
**hoho**
