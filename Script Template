//scriptName.js
//      Description:
//      Describe what the script does in general
​
//Inputs
//@ui {"widget":"separator"}
//@ui {"widget":"label", "label":"Sample Separator #1"}
//@input SceneObject SampleObject1
​
//@ui {"widget":"separator"}
//@ui {"widget":"label", "label":"Sample Separator #2"}
//@input SceneObject SampleObject2
​
//Variable declaration
var sampleVar = 0;
var sampleTransform = script.SampleObject1.getTransform();
var samplePosition;
​
//Functions
script.api.sampleApiFunction = function(){
    samplePosition = sampleTransform.getWorldPosition();
    sampleVar = 0;
}
​
function sampleFunction(){
    sampleVar++;
    sampleDelayedCallbackEvent.reset(2);
}
​
//Events and bindings
var sampleDelayedCallbackEvent = script.createEvent("DelayedCallbackEvent");
sampleDelayedCallbackEvent.bind(function(eventData)
{
   var sampleTransform2 = script.SampleObject2.getTransform();
   sampleTransform2.setWorldPosition(samplePosition);   
});
​
var sampleTouchEvent = script.createEvent("TouchEndEvent");
sampleTouchEvent.bind(function(eventData){
    script.SampleObject2.enabled = !script.SampleObject2.enabled;    
});
​
//Lines to execute when the script loads
sampleFunction();
​
​
​
