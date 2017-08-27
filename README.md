# summernote-ext-emoji-ajax
A summernote extension that uses the [github emoji api](https://api.github.com/emojis) and loads them via ajax.

All the other [emoji extensions](https://github.com/summernote/awesome-summernote) I tried were either old/broken or weren't doing it for me.  Mostly I had problems with the browser stalling as it loaded the images.

This extension uses the github emoji source, similar to the [Summernote Emoji Hint example](http://summernote.org/examples/#hint-for-emoji), except it uses AJAX asynch.

### Usage
1. Include the js and css
2. add `emoji` to your toolbar somewhere:

````
$('#summernote').summernote({
    toolbar: [
        ...
        ['insert', ['picture', 'link', 'emoji']]
    ]
});
````

### Example
https://jsfiddle.net/43Tesseracts/n0936z0f/

### Notes
* The emoji are sized with `em` to scale with the text style
* However, they don't yet scale if you change the font size directly using the summernote font-sze button....grrr.
* I'm still having browser delays on Firefox... Chrome seems to have no prob.
