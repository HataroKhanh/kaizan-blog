---
title: "Kaizan"
description: "Blog cá nhân của Kaizan. Nơi ghi chép những trải nghiệm về Linux, quản trị máy chủ, lập trình tự động hóa và lối sống công nghệ tối giản."
layout: layout.njk
---

# Chào, mình là Kaizan (Khanh) :)
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
