# LAM

## Feb 5 Notes
The new SLAM method incorporates equispaced points around a sphere and uses a KD neighbour solver to index a structure. BMG model still takes an incredibly long time to compute. Looking at the results the likely candidate is the fact I'm generating a lot of new motifs, that makes the search run increasingly longer. I'm broadening my point space to resolve a coarser motif. Hopefully this can speed things up. Python unfortunately isn't very friendly multi-threading, especially when the loops I'm computing are relatively simplistic, attempts to multi-task usually eat more time in memory allocation and initialization costing more time than I would save. I can also consider broadening my least squares cutoff as well.
