# LAM

## Feb 5 Notes
The new SLAM method incorporates equispaced points around a sphere and uses a KD neighbour solver to index a structure. BMG model still takes an incredibly long time to compute. Looking at the results the likely candidate is the fact I'm generating a lot of new motifs, that makes the search run increasingly longer. I'm broadening my point space to resolve a coarser motif. Hopefully this can speed things up. Python unfortunately isn't very friendly multi-threading, especially when the loops I'm computing are relatively simplistic, attempts to multi-task usually eat more time in memory allocation and initialization costing more time than I would save. I can also consider broadening my least squares cutoff as well.

## Feb 13 Notes
I adjusted my least squares error to be normalized by the square root of coordination number. I also normalize the coordinates so the least squares differences are entirely a result of angular differences rather than atomic spacing. Currently working on fine tuning reasonable cut off parameters where motifs aren't overly abundant but the resulting LAMs are sharp enough to have an evident motif.
