# AnjaliSapkota_Boose_DrawingApp
A Windows Forms–based drawing application built using the BOOSE command-processing library.
The system interprets user-written commands such as moveto, drawto, circle, rect, and pencolour, and executes them on a graphical canvas.

Project Features
✔ Custom Command Implementations

Includes fully implemented BOOSE drawing commands:

MoveTo

DrawTo

Circle

Rect

PenColour

Write

✔ Command Parser

Parses single-line and multi-line input commands and converts them into executable BOOSE commands.

✔ Program Execution Engine

Stores, compiles, and runs BOOSE programs using command objects.

✔ Canvas Renderer

A custom AppCanvas that draws shapes using WinForms graphics.

✔ Full XML Documentation

All classes and methods in both:

Main project, and

Unit testing project
are documented using XML comments.
Documentation files are generated using Visual Studio and hosted on this repository.

Unit Testing

A dedicated unit-testing project is included to verify the correctness of core BOOSE components.

The following features are covered by automated tests:

MoveToCommand

Validates parameter checking and correct coordinate updates.

DrawToCommand

Ensures proper drawing behaviour and position updates.

Single-line command execution

Verifies correct parser and runtime behaviour for individual commands.

Multi-line program execution

Tests parsing and execution of scripts with multiple commands.

These tests ensure that the main drawing workflow—moving the pen, drawing lines, and executing scripts—works as expected.
