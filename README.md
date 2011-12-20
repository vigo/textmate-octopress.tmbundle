# Octopress bundle for TextMate

This is un-offical bundle for great blogging engine for developers: 
[Octopress](http://octopress.org/).

## Download & Installation
To install via Git:

    cd "~/Library/Application Support/TextMate/Bundles"
    git clone git://github.com/vigo/textmate-octopress.tmbundle.git
    osascript -e 'tell app "TextMate" to reload bundles'

To install without Git:

    cd "~/Library/Application Support/TextMate/Bundles"
    wget ...
    tar xvzf ...
    osascript -e 'tell app "TextMate" to reload bundles'

# Plugins
## Image: img[tab]
Inserts `img` tag

    {% img [left|center|right] [/path/to/image] [width] [height]  [title] [alt]  %}

## Backtick Code Block: code[tab]
Inserts backtick code block.

    ``` [language] [title] [url] [link text]
    code here
    ```

## Inline Code Block: code[tab]
Inserts codeblock tags.

    {% codeblock [title] lang:[lang] [url] [link text] %}
    code ...
    {% endcodeblock %}

## Blockquote: quo[tab]
Inserts blockquote

    {% blockquote [author/@twitter, source] [link] [link title] %}
    Text...
    {% endblockquote %}

## Pullquote Wrapper: quo[tab]
Inserts pullquote tags. After entering your text, don't forget to select your
word/sentence to pullquote via `kntrl+p`

    {% pullquote %}
    Text...
    {% endpullquote %}

## Pullquote Puller: [kntrl+p]
Wraps selectin with `{" Text "}`. Usefull after **Pullquote Wrapper**

    {% pullquote %}
    Surround your paragraph with the pull quote tags. Then when you come to
    the text you want to pull, {" surround it like this "} and that's all there is to it.
    {% endpullquote %}    

# Other

## Excerpts
Inserts `<!-- more -->` to split the post for an excerpt.


## Pygments Language Help: [kntrl+h]
Shows the list of language syntax names via html form. For more information 
please visit [Pygments Demo Page](http://pygments.org/demo/)

## Backtick Inline: [kntrl+c]
Wraps selection with backtick.

    This is a `selection`


# Notes

* Don't forget, this bundle uses html and markdown scopes: `text.html,text.html.markdown`
