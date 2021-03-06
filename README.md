GGStick
=======

GGStick is an easy to use virtual thumb-stick module for Corona SDK powered games. You can have as many as you like all playing nicely together.

Check out the sample main.lua file for a very basic twin stick shooter, you'll want to try it on a device as it uses multitouch.

Basic Usage
-------------------------

##### Require the code
```lua
local GGStick = require( "GGStick" )
```

##### Make a basic stick
```lua
local stick = GGStick:new()
```

##### Make a customised one
```lua
local stick = GGStick:new
{
	alpha = 0.7, 
	fadeInTime = 100,
	instantResetOnRelease = true,
	outer = { path = "outer.png", width = 50, height = 50 },
	inner = { path = "inner.png", width = 10, height = 10 }
}
```

##### Print out the stick values ( via properties or functions )
```lua
print( stick.angle )
print( stick:getMagnitude() )
print( stick:getPosition().x, stick.position.y )
print( stick:getDistance() )
print( stick.origin )
print( stick.vector.x, stick:getVector().y )
```

##### Destroy the stick
```lua
stick:destroy()
stick = nil
```
