# half-planes-lua
Small library for half plane math

[![License](https://img.shields.io/badge/license-CC0--1.0-green)](LICENSE)

A Lua library for performing mathematical operations related to half planes.

## Overview

This Lua library provides functionality for working with half planes in a mathematical context. It allows you to perform various operations involving half planes, including intersection calculations, containment checks, and more.

## Features

- **Ray-to-Half-Plane Intersection**: Determine if a ray intersects a half plane and calculate the intersection point.
- **Point Containment**: Check if a point lies within a half plane.
(TODO: - **Angle Operations**: Perform angle-related calculations useful in half plane mathematics.)

## Installation

You can include this library in your Lua project by simply copying the relevant Lua files into your project directory and requiring them in your code.

## Usage

```lua
-- half planes intersection:
local halfPlane = HalfPlanesLib:new({x = 200, y = 300}, -2, 1) -- point and direction as vector (not normilized)
local halfPlane2 = HalfPlanesLib:new({x = 300, y = 200}, 1, -6)
local pointIntersection = halfPlane:getIntersectionPoint(halfPlane2)

if pointIntersection then
    print("Intersection Point:", pointIntersection.x, pointIntersection.y)
else
    print("No Intersection")
end
```




```lua
-- check if the point is inside of half plane:
local testPoint = {x = 4, y = 5}
local isInside = halfPlane:contains(testPoint)
print("Point inside the half-plane:", isInside)
```
