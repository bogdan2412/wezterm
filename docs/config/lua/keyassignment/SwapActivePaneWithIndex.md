# `SwapActivePaneWithIndex`

{{since('nightly')}}

`SwapActivePaneWithIndex` swaps the active pane with the pane with the specified
index within the current tab.  Invalid indices are ignored.

The action requires two named arguments, *pane_index* and *keep_focus*.
*pane_index* is the zero-based index of the pane to swap with.

If *keep_focus* is true, focus is retained on the currently active pane but in its
new position. If false, focus moves to the other pane, which now occupies the
original position of the active pane.

This example causes CTRL-ALT-a, CTRL-ALT-b, CTRL-ALT-c to swap the current pane
with the 0th, 1st and 2nd panes, respectively:

```lua
local wezterm = require 'wezterm'
local act = wezterm.action
local config = {}

config.keys = {
  {
    key = 'a',
    mods = 'CTRL|ALT',
    action = act.SwapActivePaneWithIndex { pane_index = 0, keep_focus = true },
  },
  {
    key = 'b',
    mods = 'CTRL|ALT',
    action = act.SwapActivePaneWithIndex { pane_index = 1, keep_focus = true },
  },
  {
    key = 'c',
    mods = 'CTRL|ALT',
    action = act.SwapActivePaneWithIndex { pane_index = 2, keep_focus = true },
  },
}

return config
```
