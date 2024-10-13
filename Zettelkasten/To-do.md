Things to do for the tile editor from game 13/10/2024
- [ ] Install and setup ImGuid
- [ ] Make a rough sketch of how the editor will function (figure out the abstractions)
	We need (somewhat ordered)
	**Interaction with the UI:**
	- Load the tilesheet within imgui
	- Figure out which tile we're getting from mouse position
	- be capable to transfer information using the mouse (somekind of clipboard memory)
	**Grid**:
	- Render the grid with vertical/horizontal lines relative do width/height
	- Attach tiles to cells
	- Remove tiles from cells
	- Paint brush tiles within cells
	- Do some kind of neighbour checking to ensure tile fits in bounds
	**Camera**
	- Move using mouse (clicking and dragging)
- Things i still need to think about:
	- Layering / Tile hierarchy
	- Some tiles must be fixed like floors but idk trees don't need a completely fixed position we might have some kind of "free"  positionable layer
	- Bucketing
	- Copy/paste
	- Undo/redo
	- Zoom-in/out
	- How to export (texture ? custom file format ?)
	- A shit ton of opengl implementation details.