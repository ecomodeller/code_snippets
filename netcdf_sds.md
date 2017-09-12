Reading NetCdf files using SDSLite

In order to read files on the network they have to be opened in ReadOnly mode.

```C#
var nc = Microsoft.Research.Science.Data.NetCDF4.NetCDFDataSet.Open(filename, ResourceOpenMode.ReadOnly);
```
