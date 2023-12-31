# gfx-10-final

Daphne Qin, Ruiwen Tang

This repo is a reupload of our original project. We are unable to make the original repo public or fork it due to the restrictions that Stuyvesant has placed on it.

To run this program, type in `make` in your terminal, and the computer will do the rest. The output will be a graduation cap.

This program uses custom `.mdl` files, which supply the instructions for the program to draw. All sample files are in `mdl_files`. To change which file is used, edit the second line of the makefile with the desired `.mdl` file.

During this project, we pair programmed on Zoom, with one person sharing their screen at a time. Due to this, there may be a disproportionate number of commits by certain people, but we did equal amounts of work.

## Implementations
- Phong Shading (always activated)
- `save_coord_system`: takes one argument for the name of this saved stack, and saves the current stack of coordinate system. If a line, box, sphere, cylinder, hollow cylinder, or torus specifies the name of this saved coordinate system later on, then the top of that saved stack will be used, rather than the current coordinate system stack.
- new primitives
  - `cylinder`: takes parameters `x, y, z, r, h`, where `(x,y,z)` is the origin of the base of the bottom circle, `r` is the radius and `h` is the height. Height increases along `y`.
    - Usage: `cylinder [constants] x y z r h [coord_system]`
  - `hollow_cylinder`: takes parameters `x, y, z, r0, r1, h`, where `(x,y,z)` is the origin of the base of the bottom circles, `r0` is the radius of the inner circle, `r1` is the radius of the outer circle, and `h` is the height. Height increases along `y`.
    - Usage: `hollow_cylinder [constants] x y z r0 r1 h [coord_system]`
