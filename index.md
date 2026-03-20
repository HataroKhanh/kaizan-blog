---
title: "Kaizan"
description: "Blog cá nhân của Kaizan. Nơi ghi chép những trải nghiệm về Linux, quản trị máy chủ, lập trình tự động hóa và lối sống công nghệ tối giản."
layout: layout.njk
---

<div style="text-align: center; margin-bottom: 2rem;">
  <img src="/images/logo.jpg" alt="Kaizan Logo" style="width: 150px; height: 150px; border-radius: 50%; border: 3px solid #eee;">
</div>

# Chào, mình là Kaizan (Khanh) :)

<div style="margin: 2rem 0;">
  <form action="https://www.google.com/search" method="get" target="_blank">
    <input type="hidden" name="sitesearch" value="kaizan.io.vn">
    <input type="text" name="q" placeholder="Tìm kiếm trên blog..." style="padding: 0.5rem; width: 80%; max-width: 400px; border: 1px solid #ccc; border-radius: 4px;">
    <button type="submit" style="padding: 0.5rem 1rem; cursor: pointer; border-radius: 4px; background: #333; color: #fff; border: none;">Tìm kiếm</button>
  </form>
</div>
...
Bạn có thể tìm hiểu thêm về [mình](/about/), [trang web này](/about/), [những gì mình đang làm](/follow/), hoặc thậm chí là [những công nghệ mình sử dụng](/uses/).

Về phần 'blog'... các bài viết gần đây nhất của mình được liệt kê dưới đây, nhưng bạn có thể tìm thấy phần còn lại của kho lưu trữ [tại đây](/blog/). Đối với các trang còn lại, hãy [khám phá thêm](/explore/).

Hy vọng bạn sẽ thích!.

Không thích thì cũng không sao :)))

---

### Bài viết gần đây:

<ul>
{% for post in collections.posts reversed limit:5 %}
  <li><a href="{{ post.url }}">{{ post.data.title }}</a></li>
{% endfor %}
</ul>
