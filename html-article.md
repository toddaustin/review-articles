#How to Input a Large Body of Text in HTML
(Category: HTML Forms)

The `<textarea>` element is used in a form to display multi-lines of text.  It must have a start tag and an end tag. A user can enter an infinite number of characters in a textarea. Text entered into a textarea is displayed in a monospaced font by default. 
```html
  <textarea>This is a textarea, it can contain multiple lines of text and will display in a monospace font.</textarea>. 
```
![Textarea](http://toddaustin.com/images/mod-dev/textarea1.jpg)  

###Textarea Attributes
Properties of a textarea are declared using attributes. Textareas can contain several different attributes in order to provide additional information about the textarea. Attributes are always specified in the start tag.
```html
<textarea cols="3">This is a textarea with the attribute cols</texarea>
```

####Types of textarea attributes:

####autofocus
The **autofocus** attribute tells the browser that when the page loads, the textarea receives focus. Giving an element focus makes it active and ready for input. Autofocus is considered a boolean attribute, meaning that adding a boolean attribute with no set value to an element will be percieved by the browser to have its value set to true. To represent false, simply omit the attribute. 
 
```html
// this textarea will have focus on page load
<textarea autofocus></textarea>
```
![autofocus](http://toddaustin.com/images/mod-dev/autofocus.jpg)  
####cols
The **cols** attribute specifies the width of a textarea. The value of the cols attribute represents the number of characters per line. The value of cols must be a positive number. If omitted, the default value of cols is 20. Width can also be set via CSS, which can override the default value.
```html
<textarea cols="60"></textarea>
```
![Cols](http://toddaustin.com/images/mod-dev/cols.jpg)  

####dirname
The **dirname** attribute sends the text direction of the textarea when the form containing the textarea is submitted. The value of dirname is made up of the name of the textarea followed by .dir. What gets sent depends on what the textarea contains. If the content is english, then the following will be sent: myArea.dir=ltr.
```html
<textarea name="myArea" dirname="myArea.dir"></textarea>
```
####disabled
The **disabled** attribute is a boolean that indicates whether or not the user can interact with the textarea. A disabled textarea will not be selectable by the user and no value will be submitted with the form. If omitted, the value of this attribute will be inherited from its parent element. When an input is disabled, the background color and font color may be different than normal, depending on the browser.
```html
<textarea disabled></textarea>
```
![Disabled](http://toddaustin.com/images/mod-dev/disabled-ie.jpg)
####form
The **form** attribute specifies the id of the form element that is the parent of, or associated with the textarea. The value must be the ID of a form element that resides in the same document as the textarea. Using this attribute allows the textarea to be placed anywhere on the page. While omitting this attribute requires the texarea to be a descendent of a form element.
```html
<textarea form="myForm"></textarea>
```
####maxlength
The **maxlength** attribute allows the form creator to set a maximum limit of characters that the user is able to enter into the textarea. If maxlength is omitted, then the user may enter an unlimited amount of characters into the textarea. 
```html
<textarea maxlength="20"></textarea>
```
![maxlength](http://toddaustin.com/images/mod-dev/maxlength.jpg)

####name
The **name** attribute gives a name to the textarea. This can be used to reference the data entered in the textarea when the form is submitted or by using javascript.
```html
<textarea name="myArea"></textarea>
```
####placeholder
The **placeholder** attribute allows a suggestion for the type of content to be entered into the textarea input. Placeholder text is displayed before the user types in their input. 
```html
<textarea placeholder="This is placeholder text"></textarea>
```
![placeholder](http://toddaustin.com/images/mod-dev/placeholder.jpg)
####readonly
The **readonly** attribute is a boolean attribute. Its use disallows modification of the textarea content. Readonly is similar to the disabled attribute, but with readonly, the user can still click into and select the content inside the textarea and the textarea value is submitted with the form.
```html
<textarea readonly></textarea>
```
![readonly](http://toddaustin.com/images/mod-dev/readonly.jpg)
####required
The **required** attribute is a boolean attribute that specifies that the user must enter content into the textarea in order for the form to be submitted.
```html
<textarea required></textarea>
```
####rows
The **rows** attribute specifies the visible height in lines for that textarea. Height can also be specified via CSS, which will override the rows attribute. If omitted, the default row value is 2.
```html
<textarea rows="40"></textarea>
```
####wrap
The **wrap** attribute specifies how the textarea text will wrap when the form is submitted. There are two possible values for the wrap attribute. When wrap="hard", linebreaks are added so that each line is no wider than the cols attribute (which must be specified as well). When wrap="soft", the text will not wrap, and no linebreaks are inserted. Soft is the default setting when the wrap attribute is omitted.
```html
<textarea wrap="hard"></textarea>
```
###Textareas are useful
The `<textarea>` element is a very useful addition to forms when you want the user to enter long form text such as comments, descriptions or summaries. Using the many attributes available for the textarea element allows for control of the textarea display as well as whether it is a required field, how much text can be entered, and whether or not the field can even be utilized by the user.
