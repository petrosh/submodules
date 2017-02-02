# submodules
Submodules and jekyll

## Add submodule

```sh
git submodule add https://github.com/petrosh/submodules-posts _posts
git submodule update --remote --merge
git commit -am "ok" && git push
```

## Add symlinks

```sh
# /
sudo ln -s submodules-main/docs _docs

# /_includes
sudo ln -s ../submodules-main/includes main
```

{% include post-list.html %}
{% for d in site.docs %}- [{{ d.title }}]({{ d.url | absolute_url }})
{% endfor %}
{% include footer.html %}
{% include main/docs-nav.html %}
