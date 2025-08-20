---
layout: home
title: "Money Talks"
permalink: /
description: "Simplified finance and economics — learn what really moves money."
author: "Money-Meaning"
image: "/assets/images/hero-money.jpg"
---

# 💰 Money Talks: An Economics Blog

Welcome to *Money Talks*, where we simplify finance and economics so you can understand **what really moves money**.

➡️ Scroll down for the latest posts!

<section class="hero" aria-labelledby="hero-heading">
  <h2 id="hero-heading" style="margin-top:0;">Latest insights, explained simply</h2>
  <p>Short, readable explainers on topics like inflation, markets, personal finance, and policy — written for curious people who want to make better money decisions.</p>
  <p><a href="/about" class="btn">About the author</a> <a href="/tags" class="btn muted">Browse topics</a></p>
</section>

<section class="recent-posts">
  <h3>Recent posts</h3>
  {% if site.posts.size > 0 %}
    <ul class="post-list">
      {% for post in site.posts limit:6 %}
      <li class="post-item">
        <a href="{{ post.url | relative_url }}">
          <strong>{{ post.title }}</strong>
        </a>
        <div class="post-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
          {% if post.tags %} • <span class="tags">{% for tag in post.tags %}<a href="/tag/{{ tag | slugify }}/" class="tag">{{ tag }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}</span>{% endif %}
        </div>
        <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      </li>
      {% endfor %}
    </ul>
    <p><a href="/blog" class="btn">See all posts</a></p>
  {% else %}
    <p>No posts yet — start by creating a post in the _posts folder.</p>
  {% endif %}
</section>

<!-- Optional: featured newsletter / CTA -->
<section class="cta">
  <h3>Get new posts by email</h3>
  <p>Subscribe to a short weekly newsletter: quick explainers, charts, and links.</p>
  <!-- Replace the action with your newsletters provider form -->
  <form action="https://example.com/subscribe" method="post" class="subscribe-form" style="display:flex; gap:0.5rem; align-items:center; flex-wrap:wrap;">
    <input type="email" name="email" placeholder="you@example.com" required style="flex:1; min-width:220px; padding:0.5rem;" />
    <button type="submit" class="btn primary" style="padding:0.5rem 1rem;">Subscribe</button>
    <!-- Secondary button linking to a newsletters directory / multi-subscribe page -->
    <a href="/newsletters" class="btn outline" style="margin-left:0.5rem; padding:0.5rem 1rem;">Subscribe to more newsletters</a>
  </form>
  <p style="margin-top:0.75rem;">Want curated topic lists or multiple options? Visit the newsletters page to pick the ones you want.</p>
</section>

<!-- Small site notes -->
<footer class="home-footer">
  <p>Want a particular topic covered? <a href="/contact">Get in touch</a>.</p>
</footer>