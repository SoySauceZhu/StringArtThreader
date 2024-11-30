# Functional Requirement
A software that takes in a picture and generate a scheme for string art.

A machine that takes in a the scheme and threading black string on a round board on which nails are smashed manually. 
 
## Specification
1. nails are labeled with numbers
2. the scheme stores the number of nails that string comes from and goes to.  
3. (not determined) The machine has two motor: one for rotating the spinning board, one for driven the hook.
4. (not determined) The board should be able to rotate to desired position (described either by nail number or degree).
5. (not determined) The hook need to thread the string only by "tick" for once. 

# Control
- Problem: The machine's working flow is very complicated.
  - 1. Jay would come up a sketch for the machine's workflow by Christmas.  

- Problem: How to control the spinning board with high precision. i.e. 360 pins will need precision better than 1 deg.
  - 1. Well designed and well adjusted closed loop controller.
  - 2. Coloring the circumference of the board with black and white color to describe the angular position. (still a feedback control system)
  - 3. Naively, using servo motor. Tell it to rotate 136 deg. (open loop system)

# Mechanical
- Problem: Do we need a gear reducer?
  - 1. Better to assemble a spinning board and try if it spins too fast or the moment is not high enough.
  - 2. We ask for a really strong motor, then no reducer needed.
  - 3. Or if AA can give advices yes / no.

- Problem: Where to customize a lever-hook mechanism for the string holder.
  - The required mechanism is simple: lever and bearing and a servo motor

# Software
The string art scheme generator is good. And there are many online applications could do so as well. (https://halfmonty.github.io/StringArtGenerator/). But anyway, Jay's software could be a part in the presentation.

The control software should be implemented after the workflow and algorithm is determined. If feedback control method is used, we need refine and adjust the parameters in the controller.

