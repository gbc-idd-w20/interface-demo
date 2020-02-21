# Problem Solving an Interactive Interface

This project's goal was to demonstrate my problem solving process for approaching an interactive interface problem. The idea was to do so with no previous experience or understanding of the actual application of logic, and without checking the inspiration interface's source code for hints.


## Inspiration

<http://www.adhamdannaway.com/> (only viewable on desktop only as it requires mouse movement)

Prototyping the "design"/"develop" hover functionality seen at the website above. This interface demo was completed at the requested of a student.


## Video Recording

[Watch a recording of the process in its entirety here](https://ca-lti.bbcollab.com/recording/86c22c9e79e4413092e3b4ab32453f0e). Note the video was recorded without sound, and at a few points I stopped to talk to students.

Throughout the video I make written notes to help the viewer better understand my thinking/process as I'm problem solving the issues that arise. _As always_, I start by summarizing my understanding and expectations, based on the limited interaction with the interface _(and you should too!)_

### Time markers for the major video milestones:

- `00:00` Summarizing the interactions
- `14:40` HTML/CSS Prototyping
- `20:05` JavaScript Prototyping
- `57:40` Adding the image assets


## To Complete the Interface

A few next steps:

- [ ] Use an image that has a transparency to create a layering effect
  - The layers can all be parallaxed
- [ ] When you "leave" the container, remove the faux width on the child element so that it snaps back to starting `width: 50%`
  - Can add a `transition` to "width" to avoid the jittery jumping and smooth it out
- [ ] Apply a partial shift to the entire container's `transform:translate()` (in the direction of the mouse) to create a parallax
  - Can use the distance from center divided by some factor (to give it a smaller shift than the foreground elements)



## Interaction Notes (written _before_ starting, captured in the video)

- An element with a background image (the "designer" side) and a child within it (the "coder" side). The coder side is cropped from the right side (50% to start). The width of the coder element is changed relative to the position of the mouse as it moves over the face container. The "coder" image is anchored to the right side of the face.
  - Might consider that the "coder" is the background image and the "designer" is the foreground, so that no right alignment is necessary (although `margin-left: auto` can probably be used without having to go into `position: absolute`)

- The width of the child is inverse to the position of the mouse. So as the mouse moves right of center, the "coder" increases it's width. As it moves left of center, the width of of the "coder" decreases relative to the position (inverse of the distance from center)

- There's also a slight sliding of the entire element at a lesser rate, again inverse of the mouse from center - giving a parallax effect.

- There's some jitter of the width when you enter the element. May be related to the movement of the container. !TODO: investigate further once I can reproduce it.