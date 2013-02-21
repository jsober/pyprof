NAME
----
pyprof - a report generator for python profiling data

SYNOPSIS
--------
`pyprof_report -d datafile [-o output_dir] [-f html] [-c 1]`

DESCRIPTION
-----------
`pyprof` generates reports from data files created using the [Python
profiler](http://docs.python.org/2.7/library/profile.html). Report data
summarizes performance by file with individual pages for each source file,
making it much easier to visualize the performance of individual functions.

OPTIONS
-------
    -d  datafile    the profiler data generated by cProfile
    -o  output_dir  the directory to which the report was generated
    -f  format      data format (currently only html is supported, which is the
                    default)
    -c  colorize    generate colorized HTML (defaults to true (1), ignored if
                    format is not html)
    -I  includes    colon-separated list of search paths
    -r  replace     colon-separated list of replacement paths; path text and
                    replacements are separated by an equal sign (=)

EXAMPLES
--------
Profile your software:

    python -m cProfile -o profiler_data my_app.py

Generate your report:

    pyprof_report -d profiler_data -o output

NOTES
-----
Only HTML format is currently supported
