#After Effects
##Wiggle

```javascript
rgb= text.animator("Animator Clr").property.fillColor.value;
hsl = rgbToHsl( rgb);
w = wiggle(0.8,100)[0];
hsl = hsl + [ w,w,0,0];
rgb = hslToRgb( hsl);
[rgb[0],rgb[1],rgb[2]]
// comment
w = wiggle( 1,100,1,0.5,textIndex*time)[0] ;
t = time /thisComp.duration; 
w * (1-t+0.5)*text.animator("Animator 1").selector("Wiggly Selector 1").maxAmount/100
maxDelay = 0; 
seedRandom(textIndex,true);
myDelay = random(maxDelay); 
t = time - myDelay;
if (t >= 0){ 
	freq =0; amplitude = 0; decay = 0;
	s = amplitude*Math.cos(freq*t*2*Math.PI)/Math.exp(decay*t);
	[s,s] 
}else{ 
	value
}
```
