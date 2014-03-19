BlinkingText
============
display.setStatusBar( display.HiddenStatusBar ) 
_W = display.contentWidth; 
_H = display.contentHeight;
local text = display.newText("Poetic of Mobile", 100, 100, "Arial", 22)
    text.x = _W/2
    text.y = _H/2
function blink()
    if(text.alpha < 1) then
        transition.to( text, {time=490, alpha=1})
	print ("1")
    else 
	print ("2")
        transition.to( text, {time=490, alpha=0.1})
    end
end
txt_blink = timer.performWithDelay(500, blink, 0)
