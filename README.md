## jQuery Text Alignment Plugin

Imagine you have worked hard to make your tables look good, but one thing keeps bugging you; the alignment of the text in the cells. You would, for example, like to align the contents of each cell on the comma character. Unfortunately, no browser supports aligning table cells on characters. This is where the jQuery Text Alignment Plugin comes in; it adds support for aligning text based on characters to all browsers.

Please keep in mind that when this plugin is used to align on characters, it will convert the children of the element it is called on to text, and apply the alignment to that. Inline markup will thus be effectively removed. Future versions of this plugin might correct this, once I figure out what to do with complex content.

The following examples selects all the cells in an example table, then uses the [jQuery Column Selector plugin](../column-selector) to select the first column, and finally aligns the cells in that column on the comma character.

    $('#example td:nth-col(1)').textAlign(',');

The `textAlign` method only accepts a single parameter, and will align all selected elements according to the same criteria. The method returns the elements it was called on, and can thus be chained.

<dl>
    <dt>textAlign(str)</dt>
    <dd>Aligns the text in the selected elements according tostrparameter. The parameter can either be one of the following keywords, or a single character:
        <dl>
            <dt>left</dt>
            <dd>Align the elements to the left.</dd>
            
            <dt>right</dt>
            <dd>Align the elements to the right.</dd>
            
            <dt>center</dt>
            <dd>Align the elements centered.</dd>
            
            <dt>justify</dt>
            <dd>Align the elements justified.</dd>
            
            <dt>start</dt>
            <dd>Align the elements according to the left-to-right locale (start means left in western languages.)</dd>
            
            <dt>end</dt>
            <dd>Align the elements according to the left-to-right locale (end means right in western languages.)</dd>
            
            <dt>&lt;character&gt;</dt>
            <dd>Align the the elements on the character. Note that elements that do not have the character are aligned as if they ended with the character. The element as a whole is aligned according to the inherited text alignment property.</dd>
        </dl></dd>
</dl>

## Example

Please see the [text alignment example page](examples/examples.html) for example code on how to use the plugin.