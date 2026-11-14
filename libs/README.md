# Bundled libraries

`owo-lib-0.13.1+26.3.jar` is a local port of [oωo](https://github.com/wisp-forest/owo-lib)
0.13.1 (MIT) to Minecraft 26.3. No upstream 26.3 build exists, and 26.2 owo jars are
binary-incompatible with the 26.3 renderer/input changes, so the UI subset used by this mod
(`ui`, `text`, minimal `mixin/ui*`/`mixin/text`) was ported and built against 26.3.

Notable deviations from upstream owo:

- blur and panorama surfaces are stubbed out (`Surface.blur`/`vanillaPanorama` return `BLANK`),
  since 26.3 removed the blur pipeline and the `GuiRenderer` cube map
- `spectrum.fsh` was updated for 26.3's `#version 330` SPIR-V shaders (explicit locations)
- cursors use `Window.selectCursor(CursorType)` instead of GLFW
- rich translation support (`owo:rich_translations`) is kept because this mod's language files
  use it; a few other owo modules (braid, config, networking, item groups) were dropped

The jar is consumed as a plain file dependency and nested into the mod jar under
`META-INF/jars/` by the `jar` task, because Loom's `include` cannot resolve local artifacts.

The remaining jars in this directory are owo's runtime dependencies. They are also nested
inside the owo jar itself; the top-level copies only exist for the development classpath.
