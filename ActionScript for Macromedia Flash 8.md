### Core ActionScript Functions:

1. trace()
- Description: Outputs messages to the Flash Output window (for debugging purposes).

2. stop()
- Description: Stops the playback of the current timeline.

3. play()
- Description: Resumes playback of the current timeline.

4. gotoAndPlay(frame)
- Description: Moves the playhead to a specified frame and continues playing from there.

5. gotoAndStop(frame)
- Description: Moves the playhead to a specified frame and stops.

6. getURL(url, window)
- Description: Opens a URL in a web browser or in a specified target window.

7. loadMovie(url, target)
- Description: Loads an external SWF or image into a movie clip or level.

8. unloadMovie()
- Description: Removes a movie or image from a movie clip or level.

9. addListener(listener)
- Description: Adds an event listener to an object (for example, button or keyboard events).

10. removeListener(listener)
 - Description: Removes an event listener from an object.

11. startDrag(target, lockCenter, left, top, right, bottom)
 - Description: Allows the user to drag an object on the stage.

12. stopDrag()
 - Description: Stops the drag action on an object.

13. duplicateMovieClip(target, newName, depth)
 - Description: Creates a duplicate of a movie clip instance.

14. removeMovieClip(target)
 - Description: Deletes a movie clip instance.

15. attachMovie(id, newName, depth)
 - Description: Attaches a symbol from the library to the stage dynamically.

16. setInterval(callback, interval)
 - Description: Calls a function or evaluates an expression at specified intervals (like a timer).

17. clearInterval(intervalID)
 - Description: Clears an interval set by the `setInterval()` function.

18. onEnterFrame = function()
 - Description: Executes a block of code every time the playhead enters a new frame.

19. _root
 - Description: Refers to the main timeline of the Flash movie.

20. _parent
 - Description: Refers to the parent movie clip of the current movie clip.

21. Math.random()
 - Description: Returns a random number between 0 and 1.

22. Math.round(value)
 - Description: Rounds a number to the nearest integer.

23. setProperty(target, property, value)
 - Description: Sets a property (like _x, _y, _alpha) of a movie clip.

24. getProperty(target, property)
 - Description: Returns the value of a movie clip’s property.

25. fscommand(command, parameters)
 - Description: Executes a command on the operating system (like quitting the projector).

26. Key.addListener(listener)
 - Description: Listens for keypress events.

27. Key.getCode()
 - Description: Returns the code of the key that was pressed.

28. Key.isDown(keyCode)
 - Description: Checks if a specific key is currently pressed.

### Event Handlers:

1. on(press)
- Description: Triggers when the user presses a mouse button on a button or movie clip.

2. on(release)
- Description: Triggers when the user releases a mouse button after pressing it on a button or movie clip.

3. on(releaseOutside)
- Description: Triggers when the user releases a mouse button outside of a button or movie clip.

4. on(rollOver)
- Description: Triggers when the mouse pointer rolls over a button or movie clip.

5. on(rollOut)
- Description: Triggers when the mouse pointer rolls out of a button or movie clip.

### Movie Clip Methods:

1. _x
- Description: Sets or retrieves the x-position of a movie clip on the stage.

2. _y
- Description: Sets or retrieves the y-position of a movie clip on the stage.

3. _width
- Description: Sets or retrieves the width of a movie clip.

4. _height
- Description: Sets or retrieves the height of a movie clip.

5. _alpha
- Description: Sets or retrieves the transparency (alpha) of a movie clip (0 to 100).

6. _rotation
- Description: Sets or retrieves the rotation angle of a movie clip.

### String Functions:

1. String.length
- Description: Returns the length of a string.

2. substring(startIndex, endIndex)
- Description: Returns a part of a string between the specified indices.

3. indexOf(substring)
- Description: Returns the position of the first occurrence of a specified substring.

4. charAt(index)
- Description: Returns the character at the specified position in a string.
