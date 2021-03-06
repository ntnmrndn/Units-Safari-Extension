#Units

Safari extension to convert imperial units embedded in text to their metric equivalent.

###Download

Download from [here](https://github.com/mirosval/Units-Safari-Extension/blob/master/units.safariextz?raw=true)

###Example

`6'2"` will be replaced with `6'2" (187.96cm)`

###Unit support

For now it supports the following conversions:

* Feet + inches to cm or m
* lbs to kg
* miles to km
* miles per gallon to litres per 100 km
* miles per hour to KM/H

###Bookmarklet

If you don't use Safari, the code still works as a bookmarklet. Created using [bookmarkleter](http://chriszarate.github.io/bookmarkleter/)

Paste the following as your bookmark URL:

    javascript:void%20function(){function%20n(n){return%22%20(%22+n+%22)%22}function%20r(n,t){if(n.nodeType===Node.TEXT_NODE)for(var%20e=0,a=t.length;a%3Ee;++e)n.nodeValue=n.nodeValue.replace(t[e].pattern,t[e].func);else%20if(n.nodeType===Node.ELEMENT_NODE)for(var%20e=0,u=n.childNodes.length;u%3Ee;++e)r(n.childNodes[e],t)}var%20t=[{pattern:/(\d+)'(\d*)(%22|''|)/g,func:function(r,t,e,a,u,o){var%20d=Math.round(100*(30.48*parseInt(t,10)+2.54*parseInt(e,10)))/100;return%20d%3E230%3Fr+n(Math.round(d)/100+%22m%22):r+n(d+%22cm%22)}},{pattern:/(\d+)ft%20%3F(\d*)in/g,func:function(r,t,e,a,u,o){var%20d=Math.round(100*(30.48*parseInt(t,10)+2.54*parseInt(e,10)))/100;return%20d%3E230%3Fr+n(Math.round(d)/100+%22m%22):r+n(d+%22cm%22)}},{pattern:/(\d+\.%3F\d*)%20%3Fpounds%3F/gi,func:function(r,t,e,a){var%20u=Math.round(45.3592*parseFloat(t))/100;return%20r+n(u+%22kg%22)}},{pattern:/(\d+\.%3F\d*)%20%3Flbs%3F/gi,func:function(r,t,e,a){var%20u=Math.round(45.3592*parseFloat(t))/100;return%20r+n(u+%22kg%22)}},{pattern:/((\d+,%3F)+\.%3F\d*)%20%3Fmiles%3F/gi,func:function(r,t,e,a){var%20t=parseFloat(t.replace(%22,%22,%22%22)),u=Math.round(160.934*t)/100;return%20r+n(u+%22km%22)}},{pattern:/(\d+\.%3F\d*)%20%3Fmpg/gi,func:function(r,t,e,a){var%20u=Math.round(100*(235.214/parseFloat(t)))/100;return%20r+n(u+%22L%20/%20100km%22)}},{pattern:/(\d+\.%3F\d*)%20%3Fmph/gi,func:function(r,t,e,a){var%20u=Math.round(160.934*parseFloat(t))/100;return%20r+n(u+%22km/h%22)}}];r(document.body,t)}();


Contributions welcome
