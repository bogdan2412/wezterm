# `tab:swap_active_pane_with_index{ pane_index, keep_focus }`

{{since('nightly')}}

Swaps the active pane with the pane corresponding to *pane_index*.
If *keep_focus* is true, focus is retained on the currently active pane but in
its new position.

The method completes after the swap and any remote layout resynchronization
finish. If *keep_focus* is false, focus stays at the original position and
transfers to the pane swapped into it. Invalid indices are ignored.

See [tab:panes_with_info](panes_with_info.md) for more information about how to
obtain pane indexes.
