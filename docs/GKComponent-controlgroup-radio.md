## controlgroup-radio
To create a set of radio buttons, add an input with a `type="radio`" attribute and a corresponding label. Set the for attribute of the label to match the id of the input so they are semantically associated.

The label element is displayed next to the radio form element. Wrap the radio buttons in a fieldset element that has a legend which acts as the title for the question.

To visually integrate multiple radio buttons into a vertically grouped button set, the framework will automatically remove all margins between buttons and round only the top and bottom corners of the set if there is a `data-role="controlgroup"` attribute on the container

### Properties
Refer to JQueryMobile's [controlgroup-radio](http://api.jquerymobile.com/checkboxradio/) Widget.

### API

- **model**：  
  	> Set data to controlgroup-radio , data type is JSON Array.
            
        var data = [{
          item: 'A'
        }, {
          item: 'B'
        }, {
          item: 'C'
        }, {
          item: 'D'
        }];

        $('#r1').gk().model(data);
          
  	> HTML template pattern {{data.key}}
  	
        <fieldset data-role="controlgroup" data-type="vertical" is="controlgroup-radio" id="r1">
          <legend>Math scores:</legend>
          <input name="degree" type="radio" value='{{score}}'>
          <label>{{item}}</label>
        </fieldset>
  	

- **apply**：  
  	> Set data to controlgroup-radio when data is only one , data type is JSON object

        var data = {
          item: 'A',
          score: 95
        };

        $('#r1').gk().apply(data);

  	> HTML template pattern {{data.key}}
  	
        <fieldset data-role="controlgroup" data-type="vertical" is="controlgroup-radio" id="r1">
          <legend>Math scores:</legend>
          <input name="degree" type="radio" value='{{score}}'>
          <label>{{item}}</label>
        </fieldset>
        
- **checked(value)**：  
  	> Select the item with the same value.  
    > Get selected value of item when value is null. 

        $('#controlgroup-radio').gk().checked();

- **unchecked(value)**：  
  	> Unselect the item with the same value.

        $('#controlgroup-radio').gk().unchecked();

- **onSelect(callback)**：  
  	> When you click on radio item , onSelect will be invoke.  
    > If set data by model API , first argument of callback is JSON object.  
    > If set data by apply API , first argument of callback is input element of JQuery.

        // If call model API , callback argument is value object
        $('#controlgroup-radio').gk().model(data);
        $('#controlgroup-radio').gk().onSelect(function(vo) {

        });

        // If call apply API , callback argument is input element of JQuery
        $('#controlgroup-radio').gk().apply(data);
        $('#controlgroup-radio').gk().onSelect(function($input) {

        });    


- **disable(rowNum)**：  
  	> Disable the item.
    > rowNum starting from 0.  
    > Disable all when rowNum is null. 

        $('#controlgroup-radio').gk().disable();
			

- **enable(rowNum)**：  
  	> Enable the item.
    > rowNum starting from 0.  
    > Enable all when rowNum is null. 

        $('#controlgroup-radio').gk().enable();

----------
Above is the description of `controlgroup-radio`. For more information, please back to [GK-Components-List](https://github.com/ezoapp/Learn-GK-Components).

EZoApp Official Site: [ezoui.com](http://ezoui.com/)




