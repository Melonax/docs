---
layout: default
permalink: /example_command
---

<!-- This must be at the beginning of your markdown description -->
{% capture description %} 

<!-- Some regular markdown -->
**Some description**   
Written purely in `markdown`, *yay*!

<!-- simple markdown list -->
- bullet point
- another bullet point
- and another one

<!-- Select all -->
<!-- Whatever you put in the text field below will be ALL selected if the user clicks anywhere on the text -->
{% include selectAll.html text="This sentence will all be selected even if the user clicks only on a single letter." %}

<!-- colored text  -->
<!-- color is the color of your text and text is the text you want to display in that color -->
{% include colored_text.html color="red" text="Some red text hello 123456" %}

<!-- table -->
<!-- find list of all table types here: https://getbootstrap.com/docs/5.0/content/tables/#variants and just change the 'primary' in table-primary to something else -->
<!-- remove w-auto if you don't wish the table to auto resize based on the text -->

| table header | another header | one more |
|-------|--------|--------|
| first | second | third |
| one | two | three |
{:class='table table-primary w-auto'} 

<!-- alert -->
<!-- find list of all alerts here: https://getbootstrap.com/docs/5.0/components/alerts/#examples and just change the type to something else -->
{% include alert.html text="Some important alert text" type="warning" %} 

<!-- This must be at the end of your markdown description -->
{% endcapture %} 

<!-- If you're NOT including any description, you can delete all the content between 'capture description' and 'endcapture' tags and even delete the tags themselves -->

<!-- The following line below will display the image and pastebin embed -->
<!-- src = full path to the Imgur image, i.e. https://i.imgur.com/zsxdHym.jpeg -->
<!-- title = title, will be displayed as a button and title of the modal -->
<!-- pastebin = the pastebin unique ID, NOT the whole url, i.e. https://pastebin.com/HVRnqeJx will be just HVRnqeJx -->
<!-- If you're NOT including pastebin, delete the pastebin="X" key completely
<!-- Do not change anything else -->
{% include example_public.html src="https://i.imgur.com/zsxdHym.jpeg" title="Some cool title" pastebin="9HNbNCrN" desc=description %} 
