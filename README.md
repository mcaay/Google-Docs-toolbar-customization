# Google-Docs-toolbar-customization
How to customize the Google Docs and Google Sheets toolbar?

It is possible to remove unnecessary elements in the brave browser with custom filters.
Similar thing might be possible in other browsers with extensions like uBlock origin.

Regular toolbar:
<img width="930" height="175" alt="image" src="https://github.com/user-attachments/assets/5c0357c1-8c88-4b7e-bb2c-1537103a1b30" />

After removing unnecessary elements:
<img width="925" height="175" alt="image" src="https://github.com/user-attachments/assets/cbb6ca98-84aa-41b3-8eaf-4ab99b95ebda" />

Likewise in Google Sheets - the regular toolbar:
<img width="927" height="153" alt="image" src="https://github.com/user-attachments/assets/1ec88c2d-2078-49b2-bd6c-92692a79fc9c" />

After removal:
<img width="930" height="151" alt="image" src="https://github.com/user-attachments/assets/08debdf5-f8bc-43ee-a77c-9234a1d319a2" />

***

## How to do it?

1. Go to [brave://settings/shields/filters](brave://settings/shields/filters).
2. In the "Create custom filters" section, append the following (the first block is for Google Docs, the second for Google Sheets):
```
docs.google.com###docs-omnibox-toolbar
docs.google.com###undoButton
docs.google.com###redoButton
docs.google.com###printButton
docs.google.com###spellGrammarCheckButton
docs.google.com###fontSizeDecrement
docs.google.com###fontSizeIncrement
docs.google.com###boldButton
docs.google.com###italicButton
docs.google.com###underlineButton
docs.google.com###insertLinkButton
docs.google.com###insertCommentButton
docs.google.com###insertImageButton
docs.google.com###alignButton
docs.google.com###outdentButton
docs.google.com###indentButton

docs.google.com###t-undo
docs.google.com###t-redo
docs.google.com###t-print
docs.google.com###t-bold
docs.google.com###t-italic
docs.google.com###t-align
docs.google.com###t-insert-link
docs.google.com###t-insert-doco
```
3. Customize according to your preference:
    - to bring back some button, simply delete the appropriate line from the filters above;
    - to delete even more buttons, inspect the page, find the element in the html code and in particular its `id`, and create a new filter according to the filters above.

***

## Why would that be useful?
For me, I often have 2 google docs files next to each other on one monitor.
In this case something as simple as changing text color should not require clicking the 3 dots due to buttons not fitting on the screen - if we remove useless buttons like "undo", the change color text button fits on the screen easily in this scenario.
