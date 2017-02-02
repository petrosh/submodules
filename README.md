# submodules
Submodules and jekyll

## Add submodule

```sh
git submodule add https://github.com/petrosh/submodules-posts _posts
git submodule update --remote --merge
git commit -am "ok" && git push
```

## Add symlinks

Symlinks in Jekill works for collections:

```sh
# /
sudo ln -s submodules-main/docs _docs
```

Not for includes:

```sh
# /_includes
sudo ln -s ../submodules-main/includes main
```

> The page build failed with the following error:  
  A file was included in `README.md` that is a symlink or does not exist in your `_includes` directory. For more information, see https://help.github.com/articles/page-build-failed-file-is-a-symlink/.

{% include post-list.html %}

## Live docs list

{% for d in site.docs %}- [{{ d.title }}]({{ d.url | absolute_url }})
{% endfor %}

## Included with relative link in submodule

{% include_relative submodules-main/includes/docs-nav.html %}

{% include footer.html %}
