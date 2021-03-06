# rexxc

rexxc invokes the REXX compiler to compile a REXX exec into CEXEC
format.  The REXX compiler and run-time products are required.

Author: Bill Schoen (wjs@us.ibm.com)

## Syntax

`rexxc [-cgV -o output_file] input_file`

* `-V` produces a listing on STDOUT
* `-c` is compile for syntax only, no output file is created
* `-g` adds the SLINE and TRACE options.  This is needed for execs that use
   sourceline() or any other function that needs the REXX source.
* `-o` names the output file.  Default is `.cexec` appended to input_file
   The permissions are preserved for an existing output file or set
   from the permissions of the original for a new file.

`input_file` is the name of the REXX program to be compiled.  Only one
           file can be specified.

## Install

   `rexxc` must be installed in the HFS.
   Download rexxc.rexx in text mode and copy it to an HFS directory
   where programs can be run.  Permissions should be at least
   read+execute, 755 is recommended.
