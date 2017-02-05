# Fast density clustering
Python code for clustering two dimensional data using kernel density maps to construct a density graph. Examples for gaussian mixtures is given.
Our algorithm solves multiscale problems (multiple variances and population sizes) and works for non-convex structures. It uses cross-validation and is regularized by two main global parameters : a neighborhood
size and a noise threshold measure. The later detects spurious cluster centers while the former guarantees that only local information is used to infer cluster centers (we avoid using long distance information). The underlying code is based on fast kd-trees nearest-neighbor searches O(nlog n) and hash tables (O(1) insertion and item search). The codes runs for large datasets (for N=10000, run time is 2-3 seconds). More coming soon ...

# Running

Clone or download this repository and run the following command inside the top directory:

```
pip3 install .
```
That's it ! 
# Examples
Check out the example for gaussian mixtures (example.py). You should be able to run it directly. It
should produce a plot similar to this: ![alt tag](https://github.com/alexandreday/fast_density_clustering/blob/master/example/result.png)

In another example (example2.py), the algorithm is benchmarked against some sklearn datasets (note that the same parameters across all datasets) : ![alt tag](https://github.com/alexandreday/fast_density_clustering/blob/master/example/sklearn_datasets.png)
# Citation

If you use this code in a scientific publication, I would appreciate citation/reference to this repository
