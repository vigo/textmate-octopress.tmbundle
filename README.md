# Octopress bundle for TextMate
This is un-offical bundle for great blogging engine for developers: 
[Octopress][octopress].

# Warning
This bundle is designed for bootstrap v1.4. Not ready for v2.0.

## Download & Installation
To install via Git:

    cd "~/Library/Application Support/TextMate/Bundles"
    git clone git://github.com/vigo/textmate-octopress.tmbundle.git
    osascript -e 'tell app "TextMate" to reload bundles'

To install without Git:

    mkdir -p ~/Library/Application\ Support/TextMate/Bundles
    # if this is the first time for bundle installation
    
    cd ~/Library/Application\ Support/TextMate/Bundles
    curl -L https://github.com/vigo/textmate-octopress.tmbundle/tarball/master | tar xz
    mv vigo-textmate-octopress.* textmate-octopress.tmbundle
    osascript -e 'tell app "TextMate" to reload bundles'

# Plugins
---
## Image: img[tab]
Inserts `img` tag. More [Octopress Help][img-tag]

    {% img [left|center|right] [/path/to/image] [width] [height]  [title] [alt]  %}


## Backtick Code Block: code[tab]
Inserts backtick code block. More [Octopress Help][code].

    ``` [language] [title] [url] [link text]
    code here
    ```


## Inline Code Block: code[tab]
Inserts `codeblock` tag. More [Octopress Help][code].

    {% codeblock [title] lang:[lang] [url] [link text] %}
    code ...
    {% endcodeblock %}


## Gist: gist[tab]
Inserts `gist` block. More [Octopress Help][code].

    {% gist [gist_id] [filename] %}


## Include Code: code[tab]
Inserts `include_code` tag. File location depends on `_config.yml`
**code_dir** value. Default is: **downloads/code**. More [Octopress Help][code].

    {% include_code [title]  [language]  [filename] %}

Example from [Octopress Help][include-code]' help:

    {% include_code Add to_fraction for floats ruby/test.rb %}

Means, `source/downloads/code/ruby/test.rb`

## Blockquote: quo[tab]
Inserts `blockquote` tag. More [Octopress Help][blockquote]

    {% blockquote [author/@twitter, source] [link] [link title] %}
    Text...
    {% endblockquote %}


## Pullquote Wrapper: quo[tab]
Inserts `pullquote` tag. After entering your text, don't forget to select your
word/sentence to pullquote via `kntrl+p`. For more information visit 
[Octopress Help][pull-quote]

    {% pullquote %}
    Text...
    {% endpullquote %}


## Pullquote Puller: [kntrl+p]
Wraps selection with `{" Text "}`. Usefull after **Pullquote Wrapper**. 
For more information visit [Octopress Website][pull-quote]

    {% pullquote %}
    Surround your paragraph with the pull quote tags. Then when you come to
    the text you want to pull, {" surround it like this "} and that's all there is to it.
    {% endpullquote %}    


## Render Partial: render[tab]
Inserts `render_partial` tag. More [Octopress Website][render-partial].
The `render_partial` tag resolves paths to the `source` directory, so write your paths accordingly.

    {% render_partial [/path/file.markdown] %}
    {% render_partial about/index.markdown %} # means: source/about/index.markdown


## Video: video[tab]
Inserts `video` tag. More [Octopress Website][video-tag]

    {% video [url] [width] [height] [url/to/poster] %}

## Vimeo: vimeo[tab]
Inserts vimeo tag. More [Gosuke Miyashita's blog][pl-vimeo]

    {% vimeo video_id width height %}

## jsFiddle: jsfiddle[tab]
Inserts jsfiddle tag. [Click here][jsfiddle] for examples.

    {% jsfiddle shorttag [tabs] [skin] [height] [width] %}


# Other
---
## Backtick Inline: [kntrl+c]
Wraps selection with backtick.

    This is a `selection`

## Liquid Syntax Wrapper: [kntrl+r]
Wraps selection with **{% raw %}** **{% endraw %}** tags to use Liquid syntax.

## Pygments Language Help: [kntrl+h]
Shows the list of language syntax names via html form. For more information 
please visit [Pygments Demo Page][pygments]


## Excerpts
Inserts `<!-- more -->` to split the post for an excerpt.



# Notes
---
* Don't forget, this bundle uses html and markdown scopes: `text.html, text.html.markdown and text.html.textile`
* User raw wrapper `kntrl+r` to publish Liquid syntax. 
* Check out [HISTORY.md](https://github.com/vigo/textmate-octopress.tmbundle/blob/master/HISTORY.md) for change log.

[octopress]: http://octopress.org/
[code]: http://octopress.org/docs/blogging/code/
[img-tag]: http://octopress.org/docs/plugins/image-tag/
[include-code]: http://octopress.org/docs/plugins/include-code/
[blockquote]: http://octopress.org/docs/plugins/blockquote/
[pull-quote]: http://octopress.org/docs/plugins/pullquote/
[render-partial]: http://octopress.org/docs/plugins/render-partial/
[video-tag]: http://octopress.org/docs/plugins/video-tag/
[pygments]: http://pygments.org/demo/
[pl-vimeo]: http://mizzy.org/blog/2011/10/30/vimeo-tag-plugin/ "Vimeo Plugin"
[jsfiddle]: http://octopress.org/docs/plugins/jsfiddle-tag/