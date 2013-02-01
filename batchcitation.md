# [NCBI Batch Citation Matcher](http://www.ncbi.nlm.nih.gov/pubmed/batchcitmatch)

## Conversion
input format:

    journal_title|year|volume|first_page|author_name|your_key|

### RegExp
```regex
^([^.]+)\. ([^.]+)\. ([^.]+)\. (\d+)( \w+)?;(\d+)(?:\((\d+)\))?:(\d+)(?:[-–](\d+))?.*
```

### Replacement
```regex
\3|\4|\6|\8|||
```

### Example
    Rotz LD, Khan AS, Lillibridge SR, Ostroff SM, Hughes JM. Public health assessment of potential biological terrorism agents. Emerg Infect Dis. 2002 Feb;8(2):225–230. http://¬dx.doi.org/¬10.3201/¬eid0802.010164.

turns into:

    Emerg Infect Dis|2002|8|225|||

and NCBI returns (via Email):

    Emerg Infect Dis|2002|8|225|||11897082
