---
layout: post
permalink: /2016/
title:  "Welcome to Jekyll!"
date:   2016-03-13 10:43:23 +0900
categories: jekyll update
---
<pre>
<code>
깃허브에 블로그 페이지 만들기

jekyll의 렌더링된 결과를 만들기 위해서 gh-pages에 push 해야한다.

이중 보안(2 Factor)을 사용하면 윈도우 커맨드 라인에서 인증 에러 생김.
    * 윈도우용 github 응용프로그램을 사용해서 해결.
</code>
</pre>
<code>
1. 깃허브 페이지에서 새로운 저장소(New Repository)를 만들고 클론 주소를 복사
2. 윈도우 커맨드 프로픔트에서(원하는 장소에 미리 상위 폴더 만들어 놓고) 
   * git init
   * git remote add origin 클론URL
   * git checkout --orphan gh-pages ( --orphan  master없는 저장소로 변경 )
3. 윈도우용 GitHub 프로그램으로 클론한 장소를 추가 하고 코멘트 써주고 커밋 
   - publish(처음에만) 하거나 sync 해주면 끝
</code>

[참고 홈페이지](https://nolboo.github.io/blog/2013/10/15/free-blog-with-github-jekyll/)

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
