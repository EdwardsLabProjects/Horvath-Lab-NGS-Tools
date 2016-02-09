
# RNA2DNA Installation #

RNA2DNA is available in two forms, a self-contained packaged binary
for 64-bit Linux systems, and as Python source. We recommend the
self-contained packaged binary for Linux systems.

## RNA2DNA for 64-bit Linux ##

1. Unpack the downloaded release:

```
    tar xzf RNA2DNA-1.0.10.Linux-x86_64.tgz
```

2. The RNA2DNA program is located in the bin subdirectory:

```
    ./RNA2DNA-1.0.10.Linux-x86_64/bin/RNA2DNA -h
    
    ./RNA2DNA-1.0.10.Linux-x86_64/bin/RNA2DNA
```

3. Test the install using the provided example data:

```
    cd RNA2DNA-1.0.10.Linux-x86_64
    ./bin/RNA2DNA -r "data/example-*.bam" -s "data/example-SNV.tsv" -o testing
```

## Python 2.7 RNA2DNA ##

1. Unpack the downloaded release:

```
    tar xzf RNA2DNA-1.0.10.Python-2.7.tgz
```

2. Locate your Python binary and ensure it is version 2.7:

```
    python --version

    /path/to/python27 --version
```

   We refer to the Python binary as `python` below, please substitute
   whatever path and version numbers are required to run Python 2.7 on
   your system. We recommend the Enthought Python Distribution (EPD) which
   pre-installs all by the pysam third-party dependencies needed by RNA2DNA.

3. Ensure the necessary third-party Python modules are installed. pysam version >= 0.8.1 is required. 

```
    pysam, numpy, scipy
```

   For the configuration and execution GUI (optional):
   
```
    wx
```

   For Excel format SNV input files (optional):

```
    xlrd, openpyxl
```

   The existence of required modules can be tested as follows:

```
    python27 -c "from scipy import __version__; print __version__"
```

4. The RNA2DNA program is located in the src subdirectory:

```
    python ./RNA2DNA-1.0.10.Python-2.7/src/RNA2DNA.py -h
    
    python ./RNA2DNA-1.0.10.Python-2.7/src/RNA2DNA.py
```

5. Test the installation using the provided example data:

```
    cd RNA2DNA-1.0.10.Python-2.7
    python ./src/RNA2DNA.py -r "data/example-*.bam" -s "data/example-SNV.tsv" -o testing
```

## See Also

[RNA2DNA Home](..), [RNA2DNA Usage] (Usage.md), [Input Files](InputFiles.md), [Output Files](OutputFiles.md), [Annotation Files](AnnotationFiles.md)