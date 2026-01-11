# AnjaliSapkota_Boose_DrawingApp

A Windows Forms–based drawing application built using the **BOOSE command-processing library**.  
The system interprets user-written commands such as `moveto`, `drawto`, `circle`, `rect`, `square`, `triangle`, `pencolour`, and `write`, and executes them on a graphical canvas.

---

## Project Features

### Custom Command Implementations
Includes fully implemented BOOSE drawing commands:
- `MoveTo`
- `DrawTo`
- `Circle`
- `Rect`
- `Square`
- `Triangle`
- `PenColour`
- `Write`

###  Command Parser
- Parses single-line and multi-line input commands
- Converts them into executable BOOSE command objects

###  Program Execution Engine
- Stores, compiles, and runs BOOSE programs using command objects

###  Canvas Renderer
- A custom `AppCanvas` that draws shapes using WinForms graphics

###  Full XML Documentation
- All classes and methods in both:
  - Main project
  - Unit testing project
- Documentation files generated using Visual Studio

### Unit Testing
A dedicated unit-testing project verifies the correctness of core BOOSE components.  
Automated tests cover:
- `MoveToCommand` – Validates parameter checking and correct coordinate updates
- `DrawToCommand` – Ensures proper drawing behaviour and position updates
- Single-line command execution – Verifies correct parser and runtime behaviour
- Multi-line program execution – Tests parsing and execution of scripts with multiple commands

These tests ensure that the main drawing workflow—moving the pen, drawing lines, and executing scripts—works as expected.

---

## Drawing Commands
- `MoveTo(x, y)` – Move the pen to coordinates `(x, y)`  
- `DrawTo(x, y)` – Draw a line from the current position to `(x, y)`  
- `Circle(radius)` – Draw a circle at the current pen position  
- `Rect(width, height)` – Draw a rectangle with specified width and height  
- `Square(size)` – Draw a square with all sides equal to `size`  
- `Triangle(x1, y1, x2, y2, x3, y3)` – Draw a triangle connecting three points  
- `PenColour(color)` – Change the pen color  
- `Write(text)` – Display text on the canvas  

**Notes:**  
- `Rect` – two parameters (width, height)  
- `Square` – one parameter (size), equivalent to `Rect(size, size)`  
- `Triangle` – three points; can also be adapted to base/height if supported  

---

## Execution Engine & Parser
- Handles single-line and multi-line BOOSE programs
- Supports variables, control structures (`if`, `for`, `while`), and custom methods

---

## Canvas Renderer
- `AppCanvas` handles all drawing operations
- Uses WinForms Graphics for rendering shapes

---

## Unit Testing
- Located in the `UnitTests` project
- Tests cover:
  - Pen movement and drawing commands
  - Parsing of single and multi-line programs
  - Variables and control flow commands
- All tests documented with XML comments
- Run tests via Visual Studio Test Explorer

---

## Design Patterns
- **Factory Pattern** – Command creation handled via a command factory  
- **Singleton Pattern** – Used for shared objects like `AppCanvas` or Execution Engine  
- **Strategy/Observer Pattern** – Demonstrated in the command execution flow  

---

## Documentation Index

### Main Application
- [Form](Form.html)  
- [AppCanvas](AppCanvas.html)  
- [VariablesStore](VariablesStore.html)  
- [SimpleParser](SimpleParser.html)  
- [MyCommandFactory](MyCommandFactory.html)  

### Drawing Commands
- [MoveToCommand](MoveToCommand.html)  
- [DrawToCommand](DrawToCommand.html)  
- [CircleCommand](CircleCommand.html)  
- [RectCommand](RectCommand.html)  
- [SquareCommand](SquareCommand.html)  
- [TriangleCommand](TriangleCommand.html)  
- [PenColourCommand](PenColourCommand.html)  
- [WriteCommand](WriteCommand.html)  

### Control / Logic Commands
- [IfCommand](IfCommand.html)  
- [ElseCommand](ElseCommand.html)  
- [EndIfCommand](EndIfCommand.html)  
- [ForCommand](ForCommand.html)  
- [EndForCommand](EndForCommand.html)  
- [WhileCommand](WhileCommand.html)  
- [EndWhileCommand](EndWhileCommand.html)  
- [MethodCommand](MethodCommand.html)  

### Data / Utility Commands
- [IntCommand](IntCommand.html)  
- [RealCommand](RealCommand.html)  
- [ArrayCommand](ArrayCommand.html)  
- [PeekCommand](PeekCommand.html)  
- [PokeCommand](PokeCommand.html)  

### Unit Testing
- [AppCanvasTests](UnitTesting/AppCanvasTests.html)  
- [CommandTests](UnitTesting/CommandTests.html)  
- [CircleCommandTests](UnitTesting/CircleCommandTests.html)  
- [DrawToCommandTests](UnitTesting/DrawToCommandTests.html)  
- [ForCommandTests](UnitTesting/ForCommandTests.html)  
- [IfCommandTests](UnitTesting/IfCommandTests.html)  
- [MethodCommandTests](UnitTesting/MethodCommandTests.html)  
- [MoveToCommandTests](UnitTesting/MoveToCommandTests.html)  
- [PenColourCommandTests](UnitTesting/PenColourCommandTests.html)  
- [RecCommandTests](UnitTesting/RecCommandTests.html)  
- [SquareCommandTests](UnitTesting/SquareCommandTests.html)  
- [TriangleCommandTests](UnitTesting/TriangleCommandTests.html)  
- [VariableStoreTests](UnitTesting/VariableStoreTests.html)  
- [WhileCommandTests](UnitTesting/WhileCommandTests.html)  

 **Note:** Each link points to the HTML documentation file generated from XML comments in the project. Open the links in a browser to view detailed documentation of each class or command.
