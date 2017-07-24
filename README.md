# accordion-slider
Responsive and Touch-enabled accordion for WordPress and jQuery. ... Accordion Slider is fully responsive and even allows you to change the layout of the accordion for different screen sizes. ... The accordion slider can be navigated by keyboard or mouse wheel.
```javascript
var jssor_1_SlideshowTransitions = [
  {$Duration:1200,$Opacity:2}
];

var jssor_1_options = {
  $AutoPlay: true,
  $SlideshowOptions: {
    $Class: $JssorSlideshowRunner$,
    $Transitions: jssor_1_SlideshowTransitions,
    $TransitionsOrder: 1
  },
  $ArrowNavigatorOptions: {
    $Class: $JssorArrowNavigator$
  },
  $BulletNavigatorOptions: {
    $Class: $JssorBulletNavigator$
  }
};
```

## TODOS
- [x] Fix responsive issue
- [ ] Modify interface

## Change Log
1. Fix responsive issue
2. Modify README

```javascript
            var jssor_1_slider = new $JssorSlider$("jssor_1", jssor_1_options);

            /*responsive code begin*/
            /*you can remove responsive code if you don't want the slider scales while window resizing*/
            function ScaleSlider() {
                var refSize = jssor_1_slider.$Elmt.parentNode.clientWidth;
                if (refSize) {
                    refSize = Math.min(refSize, 600);
                    jssor_1_slider.$ScaleWidth(refSize);
                }
                else {
                    window.setTimeout(ScaleSlider, 30);
                }
            }
            ScaleSlider();
            $Jssor$.$AddEvent(window, "load", ScaleSlider);
            $Jssor$.$AddEvent(window, "resize", ScaleSlider);
            $Jssor$.$AddEvent(window, "orientationchange", ScaleSlider);
            /*responsive code end*/
        };
```