# submodules
Submodules and jekyll

## flow

```sh
git submodule add https://github.com/petrosh/submodules-posts _posts
git submodule update --remote --merge
git commit -am "ok" && git push
```

## posts

{% for p in site.posts %}- {{ p.title }}
{% endfor %}

<script type="text/javascript">
document.body.classList.add('markdown-body'); 
</script>
