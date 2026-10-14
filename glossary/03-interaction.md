# Interaction

Events, UI states, gestures, animation, and execution controls.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## Input & states

| Term | Definition | Example |
| --- | --- | --- |
| <a id="click"></a>**Click** | A pointer activation event, commonly triggered by a mouse button. | Click a Save button |
| <a id="tap"></a>**Tap** | A brief touch interaction that activates an element. | Tap a mobile card |
| <a id="double-click"></a>**Double Click** | Two quick consecutive clicks recognized as one gesture. | Open a desktop file |
| <a id="long-press"></a>**Long Press** | Holding contact for a duration to trigger an alternate action. | Open a context menu |
| <a id="hover"></a>**Hover** | A state in which a pointing device is over an element. | Highlight a menu item |
| <a id="focus"></a>**Focus** | The state of an element currently receiving keyboard or other directed input. | Focus a text field |
| <a id="focus-visible"></a>**Focus Visible** | A focus state for which the browser determines a visible indicator is appropriate. | :focus-visible styling |
| <a id="active-state"></a>**Active State** | An activation state; CSS :active refers to an element being activated, such as while pressed. | Pressed button feedback |
| <a id="disabled-state"></a>**Disabled State** | A state preventing a control from being operated. | Submit button before form completion |
| <a id="readonly-state"></a>**Readonly State** | An input state allowing reading but not editing its value. | Read-only account ID |
| <a id="selected-state"></a>**Selected State** | A state marking an item as chosen from a set. | Selected tab |
| <a id="swipe"></a>**Swipe** | A directional touch gesture across a surface. | Swipe a carousel |
| <a id="drag-and-drop"></a>**Drag and Drop** | Moving an item by dragging it to a drop target. | Reorder list items |
| <a id="pointer-event"></a>**Pointer Event** | An event family that unifies mouse, pen, and touch pointer input. | pointerdown |
| <a id="touch-event"></a>**Touch Event** | An event reporting changes in one or more touch contacts. | touchstart |
| <a id="keyboard-event"></a>**Keyboard Event** | An event reporting key presses and releases. | keydown |

## Event handling

| Term | Definition | Example |
| --- | --- | --- |
| <a id="event-bubbling"></a>**Event Bubbling** | The phase in which an event travels from its target through ancestors. | Card receives child click |
| <a id="event-capturing"></a>**Event Capturing** | The phase in which an event travels down the ancestor chain to its target. | Capture-phase listener |
| <a id="event-delegation"></a>**Event Delegation** | Handling child element events through a shared ancestor listener. | Click handling for dynamic rows |
| <a id="prevent-default"></a>**Prevent Default** | Cancelling an event's browser-defined default action when permitted. | Prevent normal form submission |
| <a id="stop-propagation"></a>**Stop Propagation** | Stopping an event from continuing through its propagation path. | Prevent parent click reaction |

## Timing & repeat protection

| Term | Definition | Example |
| --- | --- | --- |
| <a id="debounce"></a>**Debounce** | Delaying execution until a specified quiet period follows the most recent event. | Search after typing stops |
| <a id="throttle"></a>**Throttle** | Limiting how often a function can execute during repeated events. | Scroll position tracking |
| <a id="leading-edge"></a>**Leading Edge** | Executing a rate-controlled callback at the start of an event burst. | Respond to first click immediately |
| <a id="trailing-edge"></a>**Trailing Edge** | Executing a rate-controlled callback at the end of an event burst. | Process the final typed value |
| <a id="cooldown"></a>**Cooldown** | Disallowing a repeated action for a fixed period after execution. | Resend-code timer |
| <a id="double-submit-guard"></a>**Double-submit Guard** | Blocking a duplicate submission while the previous submission is still in progress. | Disable Pay while pending |

## Animation & motion

| Term | Definition | Example |
| --- | --- | --- |
| <a id="transition"></a>**Transition** | Interpolating CSS property values when they change. | Hover color transition |
| <a id="animation"></a>**Animation** | Changing visual properties over a defined timeline. | Entrance animation |
| <a id="keyframe"></a>**Keyframe** | A declared property state at a specific point in an animation. | @keyframes fade-in |
| <a id="easing"></a>**Easing** | A function controlling how animation progress changes over time. | ease-in-out |
| <a id="spring-animation"></a>**Spring Animation** | Animation driven by an approximation of spring and damping physics. | Bouncy drawer motion |
| <a id="transform"></a>**Transform** | Visual translation, scaling, rotation, or skew without altering document flow. | transform: translateX() |
| <a id="fade"></a>**Fade** | Appearance or disappearance through opacity changes. | Fade out a dialog |
| <a id="slide"></a>**Slide** | Entrance, exit, or movement achieved by shifting position. | Bottom sheet slides up |
| <a id="microinteraction"></a>**Microinteraction** | A small response to a single user action, communicating status or feedback. | Heart animation after Like |
| <a id="reduced-motion"></a>**Reduced Motion** | Adapting motion to a user's preference for less animation. | prefers-reduced-motion |
| <a id="scroll-snap"></a>**Scroll Snap** | Aligning scrolled content to predefined stopping positions. | Snapping gallery panels |
| <a id="scroll-lock"></a>**Scroll Lock** | Temporarily preventing scrolling in a region, often behind an overlay. | Lock page behind modal |
| <a id="focus-trap"></a>**Focus Trap** | Restricting keyboard focus to a particular region while it is active. | Modal Tab navigation |
| <a id="outside-click"></a>**Outside Click** | Detecting pointer activity outside an active panel. | Dismiss open popover |
| <a id="optimistic-feedback"></a>**Optimistic Feedback** | Showing an expected successful result before the server confirms it. | Instant Like highlight |
| <a id="haptic-feedback"></a>**Haptic Feedback** | Providing tactile feedback, such as vibration, after an action. | Phone confirmation pulse |
| <a id="gesture-conflict"></a>**Gesture Conflict** | When two gesture recognizers compete for the same movement. | Horizontal swipe versus vertical scroll |
| <a id="touch-target"></a>**Touch Target** | The interactive area available for touch activation. | Increase a small icon's hit area |

For related articles and official documentation, see [References](../REFERENCES.md).
