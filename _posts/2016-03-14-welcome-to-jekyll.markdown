---
layout: post
permalink: /2016/
title:  "Welcome to Jekyll!!!"
date:   2016-03-13 10:43:23 +0900
categories: jekyll update
---
깃허브에 블로그 페이지 만들기

{% highlight bash %}
~ $ jekyll build
# => ./_site 에 현재 폴더의 내용으로 사이트를 생성합니다

~ $ jekyll build --destination <destination>
# => <destination> 에 현재 폴더의 내용으로 사이트를 생성합니다

~ $ jekyll build --source <source> --destination <destination>
# => <destination> 에 <source> 폴더의 내용으로 사이트를 생성합니다

~ $ jekyll build --watch
# => ./_site 에 현재 폴더의 내용으로 사이트를 생성하고,
#    변경사항을 감지하면 자동으로 다시 생성합니다.
{% endhighlight %}

{% highlight bash %}
# jekyll의 렌더링된 결과를 만들기 위해서 gh-pages에 push 해야한다.

# 이중 보안(2 Factor)을 사용하면 윈도우 커맨드 라인에서 인증 에러 생김.
#    * 윈도우용 github 응용프로그램을 사용해서 해결.
{% endhighlight %}


`1. 깃허브 페이지에서 새로운 저장소(New Repository)를 만들고 클론 주소를 복사`

`2. 윈도우 커맨드 프롬프트에서(원하는 장소에 미리 상위 폴더 만들어 놓고)` 

   `* git init`

   `* git remote add origin 클론URL`

   `* git checkout --orphan gh-pages ( --orphan  master없는 저장소로 변경 )`

`3. 윈도우용 GitHub 프로그램으로 클론한 장소를 추가 하고 코멘트 써주고 커밋` 

   `* publish(처음에만) 하거나 sync 해주면 끝`


[참고홈페이지](https://nolboo.github.io/blog/2013/10/15/free-blog-with-github-jekyll/)


<div class="note">
  <h5>ProTip™: 한글(cp949) 프롬프트에서 테스트시</h5>
  <p>
    커맨드 프롬프트에서 UTF-8 코드 페이지로 변경 해야 하는데 변경 방법은
    <br>` chcp 65001 ` 로 입력하면 UTF-8 코드페이지로 변경.
  </p>
</div>

<div class="note info">
  <h5>페이지 나누기는 오직 HTML 파일에서만 작동합니다</h5>
  <p>
    페이지 나누기는 Markdown 이나 Textile 파일에서는 작동하지 않습니다. 오직
    HTML 파일 안에서 사용될 때에만 작동합니다. 보통 이 기능은 포스트 목록에
    사용하기 때문에, 큰 문제가 되지는 않을 것입니다.
  </p>
</div>

<div class="note warning">
  <h5>첫 페이지 경계조건을 주의하세요</h5>
  <p>
    Jekyll 은 'page1' 폴더를 생성하지 않기 때문에, 위 코드는 ` /page1 `
    링크에 대하여 올바르게 작동하지 않습니다. 만약 이것이 문제가 된다면 아래의
    방법을 참고하세요.
  </p>
</div>

<div class="note unreleased">
  <h5>이 표시는 아직 릴리스 되지 않는 기능을 가리킵니다</h5>
  <p>이 웹사이트는 아직 릴리스 되지 않는 버전에 대한 내용도 일부 포함하고
    있습니다.</p>
</div>

Hey, folks! Bunch of bug fixes here. Notables:

* Only superdirectories of `_posts` will be categories.
* `:title` in permalink templates are now properly cased as before
* `.jekyll-metadata` being erroneously written when not using incremental build.
* Failure in liquid will now always fail the `jekyll` process.
* All hooks should now be properly registered & documented

And a bunch more changes which you can see over in the
[changelog](/docs/history).


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
