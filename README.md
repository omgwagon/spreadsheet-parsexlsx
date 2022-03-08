# NAME

Spreadsheet::ParseXLSX - parse XLSX files

# VERSION

version 0.28

# SYNOPSIS

    use Spreadsheet::ParseXLSX;

    my $parser = Spreadsheet::ParseXLSX->new;
    my $workbook = $parser->parse("file.xlsx");
    # see Spreadsheet::ParseExcel for further documentation

# DESCRIPTION

This module is an adaptor for [Spreadsheet::ParseExcel](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel) that reads XLSX files.
For documentation about the various data that you can retrieve from these
classes, please see [Spreadsheet::ParseExcel](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel),
[Spreadsheet::ParseExcel::Workbook](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel%3A%3AWorkbook), [Spreadsheet::ParseExcel::Worksheet](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel%3A%3AWorksheet),
and [Spreadsheet::ParseExcel::Cell](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel%3A%3ACell).

# METHODS

## new(%opts)

Returns a new parser instance. Takes a hash of parameters:

- Password

    Password to use for decrypting encrypted files.

## parse($file, $formatter)

Parses an XLSX file. Parsing errors throw an exception. `$file` can be either
a filename or an open filehandle. Returns a
[Spreadsheet::ParseExcel::Workbook](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel%3A%3AWorkbook) instance containing the parsed data.
The `$formatter` argument is an optional formatter class as described in [Spreadsheet::ParseExcel](https://metacpan.org/pod/Spreadsheet%3A%3AParseExcel).

# AUTHOR

Jesse Luehrs <doy@tozt.net>

# COPYRIGHT AND LICENSE

This software is Copyright (c) 2022 by Jesse Luehrs.

This is free software, licensed under:

    The MIT (X11) License
