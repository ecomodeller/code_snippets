# Netcdf Operators

Extract metadata

```
ncks -M file.nc
```

Extract variable metadata

```
ncks -m file.nc
```



Append variables

```
ncks -A file1.nc file2.nc
ncks -A file2.nc file3.nc
```

Extract hyperslab (subset) and append

```
ncks -A -d depth,1,10 MyGlobalTEM\2017090400F000.nc surf.nc
ncks -A -d depth,1,10 MyGlobalSAL\2017090400F000.nc surf.nc
```

