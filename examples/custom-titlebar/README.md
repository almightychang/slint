# Custom Title Bar

A frameless window (`no-frame: true`) with rounded corners, a drop shadow, and a fully custom title bar,
all built from ordinary Slint elements: drag the bar to move the window (`WindowMoveArea`), drag the window
edges to resize it (`resize-border-width`), double-click the bar to maximize, and use the minimize / maximize /
close buttons.

The window background is transparent and the visible "window" is a rounded rectangle drawn inset from the window
edges. The transparent margin leaves room for the shadow and doubles as an easy-to-grab resize border, and both
disappear while the window is maximized, like native decorations do.

Run it natively to see the real window behavior:

```sh
cargo run -p slint-viewer -- examples/custom-titlebar/custom-titlebar.slint
```

Moving the window requires a backend and platform with support for it (winit on Windows, macOS, X11, and Wayland;
Qt), and `resize-border-width` is winit-only for now. In the browser preview the window-management features do
nothing.

[Online code editor](https://slint.dev/snapshots/master/editor/index.html?load_url=https://raw.githubusercontent.com/slint-ui/slint/master/examples/custom-titlebar/custom-titlebar.slint)
