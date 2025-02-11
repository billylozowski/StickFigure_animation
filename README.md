# StickFigure_animation
This code generates stick figure animations from joint position data. It also produces figures for each specified event.

Chunk:
1. calls the required library packages.
2. Loads both the .txt file with position data, and a .csv with event indices.
  - if event indices are not known, use chunk 3. Otherwise, you can either manually imput event indices (chunk 4), or pull them from the loaded .csv
3. Calculate event indices from "Event" columns in current .txt file (skip if events .csv is imported)
4. Manually input known event indices for current .txt file (skip if events .csv is loaded)
5. Extract event indices from imported /csv
  - also creates a trimmed data frame from event1 (BFC) -25 to event5 (EFT) +25
  - the number of events can be adjusted as needed, as can the buffer at the start and end
6. Using the trimmed data frame, generate side-on segments plot, renders and saves the gif as the original trial name + "(side)"
  - smoother renders can be obtained by opening html file from the viewer tab
7. Using the trimmed data frame, generate front-on segments plot, renders and saves the gif as the original trial name + "(front)"
  - smoother renders can be obtained by opening html file from the viewer tab
8-12. Each of these creates a new data frame with position data from the specific event (BFC, FFC, MAW, BR, EFT), then generates a side- and front-on figure.
  - these are to be used if you want a visual for the trial's events for a presentation/manuscript
