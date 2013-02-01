# NCBI Batch Citation Matcher

## RegExp
```regex
^([^.]+)\. ([^.]+)\. ([^.]+)\. (\d+)( \w+)?;(\d+)(?:\((\d+)\))?:(\d+)(?:[-–](\d+))?.*
```

## Replacement
\3|\4|\6|\8
