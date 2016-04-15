jwysiwyg usage and api

# Introduction #

This jquery plugin is an inline content editor to allow editing rich HTML content on the fly. It's an alternative to WYMeditor with much less features. With a small file size less than 26Kb total and only 18Kb of code, the main concept is to keep it simple, not all users need font coloring or create tables, just the basic.


# jquery plugin #

jwysiwyg is compatible with jquery 1.3.2 and later (1.4.2 tested); yo can download the last jquery version from http://jquery.com/

# Quick Start #

To start using jwysiwyg just add the jwysiwyg javascript and css files on head tag in your document after jquery include


```
<script type="text/javascript" src="jquery.js"></script>
<script type="text/javascript" src="jwysiwyg/jquery.wysiwyg.js"></script>
<link rel="stylesheet" href="jwysiwyg/wysiwyg.css" type="text/css" />
```

Later just add the wysiwyg function over textarea element

```
<script type="text/javascript">
  $(function(){
      $('#wysiwyg').wysiwyg();
  });
</script>
```


# jwysiwyg customization #

For jwysiwyg customing you can use the controls variable and customize your own control buttons list.

```
  <script type="text/javascript">
(function($)
{
  $('#wysiwyg').wysiwyg({
    controls: {
      strikeThrough : { visible : true },
      underline     : { visible : true },
      
      separator00 : { visible : true },
      
      justifyLeft   : { visible : true },
      justifyCenter : { visible : true },
      justifyRight  : { visible : true },
      justifyFull   : { visible : true },
      
      separator01 : { visible : true },
      
      indent  : { visible : true },
      outdent : { visible : true },
      
      separator02 : { visible : true },
      
      subscript   : { visible : true },
      superscript : { visible : true },
      
      separator03 : { visible : true },
      
      undo : { visible : true },
      redo : { visible : true },
      
      separator04 : { visible : true },
      
      insertOrderedList    : { visible : true },
      insertUnorderedList  : { visible : true },
      insertHorizontalRule : { visible : true },

      separator07 : { visible : true },
      
      cut   : { visible : true },
      copy  : { visible : true },
      paste : { visible : true }
    }
  });
});
</script>
```

You can change your jwysiwyg configuration setting true o false to controls items

You can use the next controls:

|Control|Description|
|:------|:----------|
|strikeThrough|Strike through control Button|
|underline|Set ext underline|
|separatorXX|Insert control separator you must set XX to consecutive number|
|justifyLeft|Left text justification|
|justifyCenter|Center text justification|
|justifyRight|Right text justification|
|justifyFull|Justify text justification|
|indent |Text indent |
|outdent|Delete an indent level|
|subscript|Sub Script to numbers|
|superscript|Super script to numbers|
|undo   |Undo control|
|redo   |Redo control|
|insertOrderedList|Insert an ordered numeric list|
|insertUnorderedList|Insert an unordered list|
|insertHorizontalRule|Insert horizontal line (hr)|
|hX     |Header formatting control, you must set X between 1 to 6|
|cut    |Cut control button|
|copy   |Copy control button|
|paste  |Paste control button|

# jwysiwyg access api #

You can access and modify the jwysiwyg texarea content through next api

## Getting content ##

You can get the textarea content just using .val() method from jquery

```
   $('#wysiwyg').val();
```

## Content manipulation ##

If you want to manipulate the jwysiwyg textarea content you can use the next methods

### Insert an image ###

Insert an image on text indicator
```
$('#wysiwyg').wysiwyg('insertImage', 'http://domain.com/image.png');
```
### Insert a link ###

Insert a link over selected text
```
$('#wysiwyg').wysiwyg('createLink', 'http://google.com/');
```