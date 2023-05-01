---
author: Peter Jonson
title: Supported Functions List
description: Supported Functions List
draft: false
tags: ['SQL']
date: 2023-03-14
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

## String Functions

**AddCharLeft(Char,S,Count)**

AddCharLeft returns a string left-padded to Length with characters Char

**AddCharRight(Char,S,Count)**

AddCharRight returns a string right-padded to Length with characters Char

**RightString(S,Count)**

RightString returns the trailing characters of String up to a length of Count characters

**Replace(S,OldPattern,NewPattern)**

Replace replaces all occurrences of the OldPattern by NewPattern within the String

**SubString(S,Index,Count)**

SubString returns a substring containing Count Characters or elements starting from Index.

**LeftString(S,Count)**

LeftString returns the leading characters of String up to a length of Count characters

**MakeString(Char,Count) **

MakeString returns a string of Count filled with character Char.

**DelSpaces(S)**

DelSpaces returns string with all spaces deleted except one.
"two spaces"->"two spaces

**Delete(S,Index,Count)**

Delete removes a substring of Count characters from string S starting with S[Index]. S is a string-type variable. Index and Count are integer-type expressions. If index is larger than the length of the string or less than 1, no characters are deleted. If count specifies more characters than remain starting at the index, Delete removes the rest of the string. If count is less than or equal to 0, no characters are deleted

**DeleteCharacters(String,CharactersToDelete):String**

Deletes specific characters from the string

**DeleteLeadingCharacters(String,CharactersToDelete):String**

Deletes specific leading characters from the string

**DeleteTrailingCharacters(String,CharactersToDelete):String**

Deletes specific trailing characters from the string

**KeepCharacters(String,CharactersToKeep):String**

Deletes all characters from the string except ‘Characters To Keep’
Example: Trim(KeepCharacters(UpperCase([F1]),'1234567890'))

**Insert(Substr,Dest,Index)**

Insert merges Source into S at the position S[index]. Source is a string-type expression. S is a string-type variable of any length. Index is an integer-type expression. It is a character index and not a byte index. If Index is less than 1, it is mapped to a 1. If it is past the end of the string, it is set to the length of the string, turning the operation into an append. If the Source parameter is an empty string, Insert does nothing

**ProperCase(S)**

ProperCase returns string, with the first letter of each word in uppercase and all other letters in lowercase "proper case"->"Proper Case"

**UpperCase(S)**

UpperCase returns a string with the same text as the string passed in S, but with all letters converted to lowercase. The conversion affects only 7-bit ASCII characters between 'A' and 'Z'. To convert 8-bit international characters, use AnsiUpperCase.

**LowerCase(S)**

LowerCase returns a string with the same text as the string passed in S, but with all letters converted to lowercase. The conversion affects only 7-bit ASCII characters between 'A' and 'Z'. To convert 8-bit international characters, use AnsiLowerCase.

**AnsiUpperCase(S)**

AnsiUpperCase returns a string that is a copy of S, converted to upper case.

**AnsiLowerCase(S)**

AnsiLowerCase returns a string that is a copy of the given string converted to lower case.

**AnsiCompareStr(S1,S2)**

AnsiCompareStr compares S1 to S2, with case sensitivity.

The return value is:

{{< table "table-striped table-bordered" >}}

| Condition | Return Value |
| --------- | ------------ |
| S1 > S2   | > 0          |
| S1 < S2   | < 0          |
| S1 = S2   | = 0          |

{{< /table >}}

**AnsiCompareText(S1,S2)**

AnsiCompareText compares S1 to S2, without case sensitivity. AnsiCompareText returns a value less than 0 if S1 < S2, a value greater than 0 if S1 > S2, and returns 0 if S1 = S2.

**AnsiStrLIComp (S1,S2,MaxLen)**

AnsiStrLIComp compares S1 to S2, without case sensitivity. If S1 or S2 is longer than MaxLen characters, AnsiStrLIComp only compares up to the first MaxLen characters.

The return value is:

{{< table "table-striped table-bordered" >}}

| Condition                         | Return Value |
| --------------------------------- | ------------ |
| S1 > S2                           | > 0          |
| S1 < S2                           | < 0          |
| S1 = S2 (up to MaxLen characters) | = 0          |

{{< /table >}}

**AnsiLastChar(S)**

Call AnsiLastChar to obtain the last character in a string.

**Trim(S)**

Trim removes leading and trailing spaces and control characters from the given string S.

**TrimLeft(S)**

TrimLeft returns a copy of the string S with leading spaces and control characters removed.

**TrimRight(S)**

TrimRight returns a copy of the string S with trailing spaces and control characters removed.

**QuotedStr(S)**

Use QuotedStr to convert the string S to a quoted string. A single quote character (') is inserted at the beginning and end of S, and each single quote character in the string is repeated.

**AnsiQuotedStr(S,Quote)**

Use AnsiQuotedStr to convert a string (S) to a quoted string, using the provided Quote character. A Quote character is inserted at the beginning and end of S, and each Quote character in the string is doubled.

**AnsiExtractQuotedStr(S,Quote)**

AnsiExtractQuotedStr removes the quote characters from the beginning and end of a quoted string, and reduces pairs of quote characters within the string to a single quote character. The Quote parameter defines what character to use as a quote character. If the first character in S is not the value of the Quote parameter, AnsiExtractQuotedStr returns an empty string.

**Copy(S,Index,Count)**

S is an expression of a string or dynamic-array type. Index and Count are integer-type expressions. Copy returns a substring or sub array containing Count characters or elements starting at S[Index]. The substring or sub array is a unique copy (that is, it does not share memory with S, although if the elements of the array are pointers or objects, these are not copied as well.) If Index is larger than the length of S, Copy returns an empty string or array. If Count specifies more characters or array elements than are available, only the characters or elements from S[Index] to the end of S are returned.

**CRC16(String,Format)**

Returns CRC16 checksum of a String, Format 0=HEX ,1=Base64

**CRC24(String,Format)**

Returns CRC24 checksum of a String, Format 0=HEX ,1=Base64

**CRC32(String,Format)**

Returns CRC32 checksum of a String, Format 0=HEX ,1=Base64

**Adler32(String,Format)**

Returns Adler32 checksum of a String, Format 0=HEX ,1=Base64

**CRC64(String,Format)**

Returns CRC64 checksum of a String, Format 0=HEX ,1=Base64

**eDonkey(String,Format)**

Returns eDonkey checksum of a String, Format 0=HEX ,1=Base64

**eMule(String,Format)**

Returns eMule checksum of a String, Format 0=HEX ,1=Base64

**MD4(String,Format)**

Returns MD4 checksum of a String, Format 0=HEX ,1=Base64

**MD5(String,Format)**

Returns MD5 checksum of a String, Format 0=HEX ,1=Base64

**RIPEMD160(String,Format)**

Returns RIPEMD160 checksum of a String, Format 0=HEX ,1=Base64

**SHA1(String,Format)**

Returns SHA1 checksum of a String, Format 0=HEX ,1=Base64

**SHA224(String,Format)**

Returns SHA224 checksum of a String, Format 0=HEX ,1=Base64

**SHA256(String,Format)**

Returns SHA256 checksum of a String, Format 0=HEX ,1=Base64

**SHA384(String,Format)**

Returns SHA384 checksum of a String, Format 0=HEX ,1=Base64

**SHA512(String,Format)**

Returns SHA512 checksum of a String, Format 0=HEX ,1=Base64

**Whirlpool(String,Format)**

Returns Whirlpool checksum of a String, Format 0=HEX ,1=Base64

**GUID**

Returns GUID as a string.

About GUID

A globally unique identifier (GUID) is a unique reference number used as an identifier in computer software. The term GUID also is used for Microsoft's implementation of the Universally Unique Identifier (UUID) standard.

The value of a GUID is represented as a 32-character hexadecimal string, such as {21EC2020-3AEA-1069-A2DD-08002B30309D}, and is usually stored as a 128-bit integer. The total number of unique keys is 2128 or 3.4×1038. This number is so large that the probability of the same number being generated randomly twice is negligible

**GUIDNB**

Returns GUID without brackets and underscores (21EC20203AEA1069A2DD08002B30309D)

**StrGetLine(String,FieldNo,Delimiter,Quote):String**

Returns part of a delimited string

## Conversion Functions

**IntToStr(S)**

IntToStr converts an integer into a string containing the decimal representation of that number.

**IntToHex(I,Digits)**

IntToHex converts a number into a string containing the number's hexadecimal (base 16) representation. Value is the number to convert. Digits indicate the minimum number of hexadecimal digits to return.

**StrToInt(S)**

StrToInt converts the string S, which represents an integer-type number in either decimal or hexadecimal notation, into a number. If S does not represent a valid number, StrToInt raises an exception.

**StrToIntDef(S,Default)**

StrToIntDef converts the string S, which represents an integer-type number in either decimal or hexadecimal notation, into a number. If S does not represent a valid number, StrToIntDef returns Default.

**FloatToStr(F)**

FloatToStr converts the floating-point value given by Value to its string representation. The conversion uses general number format with 15 significant digits.

**StrToFloat(S)**

Use StrToFloat to convert a string, S, to a floating-point value. S must consist of an optional sign (+ or -), a string of digits with an optional decimal point, and an optional mantissa. The mantissa consists of 'E' or 'e' followed by an optional sign (+ or -) and a whole number. Leading and trailing blanks are ignored.

**IntegerToString(Integer)**

IntegerToString converts integer value to a string value.

**NumberToString(Float)**

NumberToString converts float value to a string value.

**StringToInteger(S)**

StringToInteger converts string value to an integer value.

**StringToNumber(S)**

StringToNumber converts string value to a float value.

## File System Functions

**FileAge(FileName)**

Call FileAge to obtain the OS timestamp of the file specified by FileName. The return value can be converted to a TDateTime object using the FileDateToDateTime function. The return value is -1 if the file does not exist.

**FileSize(FileName)**

Call FileSize to obtain the size of the file

**FileLine(FileName,LineNo)**

Call FileLine to obtain the text of LineNo

This function uses Zero Based Indexing for the LineNo Parameter

Usage Example:

```
begin
  SetVariable('<FileLine>',FileLine('C:\Test\filelist.txt',1));
  Result:=true;
end;
```

**FileExists(FileName)**

FileExists returns true if the file specified by FileName exists. If the file does not exist, FileExists returns false.

**DeleteFile(FileName)**

DeleteFile deletes the file named by FileName from the disk. If the file cannot be deleted or does not exist, the function returns false.

**RenameFile(OldFile,NewFile)**

RenameFile attempts to change the name of the file specified by OldFile to NewFile. If the operation succeeds, RenameFile returns true. If RenameFile cannot rename the file (for example, if the application does not have permission to modify the file), it returns false.

**ChangeFileExt(FileName,EXT)**

ChangeFileExt takes the file name passed in FileName and changes the extension of the file name to the extension passed in Extension. Extension specifies the new extension, including the initial dot character.
ChangeFileExt does not rename the actual file, it just creates a new file name string.

**ExtractFilePath(FileName)**

The resulting string is the leftmost characters of FileName, up to and including the colon or backslash that separates the path information from the name and extension. The resulting string is empty if FileName contains no drive and directory parts.

**ExtractFileDir(FileName)**

Extracts Directory part from the File Name provided

**ExtractFileDrive(FileName)**

ExtractFileDrive returns a string containing the drive portion of a fully qualified path name for the file passed in the FileName. For file names with drive letters, the result is in the form "drive". For file names with a UNC path, the result is in the form "\servername\sharename". If the given path contains neither style of the path prefix, the result is an empty string.

**ExtractFileName(FileName)**

The resulting string is the rightmost characters of FileName, starting with the first character after the colon or backslash that separates the path information from the name and extension. The resulting string is equal to FileName if FileName contains no drive and directory parts.

**ExtractFileExt(FileName)**

Use ExtractFileExt to obtain the extension from a file name.

**ExpandFileName(FileName)**

ExpandFileName converts the relative file name into a fully qualified path name. ExpandFileName does not verify that the resulting fully qualified pathname refers to an existing file, or even that the resulting path exists.

**ExpandUNCFileName(FileName)**

ExpandUNCFileName returns the fully-qualified file name for a specified file name.

**ExtractRelativePath(FileName)**

Call ExtractRelativePath to convert a fully qualified path name into a relative pathname. The DestName parameter specifies a file name (including path) to be converted. BaseName is the fully qualified name of the base directory to which the returned pathname should be relative. BaseName may or may not include a file name, but it must include the final path delimiter.

**DiskFree(Drive)**

DiskFree returns the number of free bytes on the specified drive, where 0 = Current, 1 = A, 2 = B, and so on.

**DiskSize(Drive)**

DiskSize returns the size in bytes of the specified drive, where 0 = Current, 1 = A, 2 = B, etc. DiskSize returns -1 if the drive number is invalid.

**GetCurrentDir(Directory)**

GetCurrentDir returns the fully qualified name of the current directory.

**SetCurrentDir(Directory)**

The SetCurrentDir function sets the current directory. The return value is true if the current directory was successfully changed, or false if an error occurred.

**CreateDir(Directory)**

CreateDir creates a new directory. The return value is true if a new directory was successfully created, or false if an error occurred.

**RemoveDir(Directory)**

Call RemoveDir to remove the directory specified by the Dir parameter. The return value is true if a new directory was successfully deleted, false if an error occurred. The directory must be empty before it can be successfully deleted.

**GetWindowsTemporaryDirectory**

The GetWindowsTemporaryDirectory function returns windows temporary path.

**GetTemporaryFile(Extension)**

The GetTemporaryFile function returns a temporary file path. The file is located in windows temporary directory

**GetTemporaryFileInDirectory(Directory,Extension)**

The GetTemporaryFileInDirectory function returns temporary file path. The file is located in the directory

**GetTemporaryDirectory(Directory)**

The GetTemporaryDirectory function returns a temporary directory name in a specified directory

**FileCRC16(String,Format)**

Returns CRC16 checksum of a File, Format 0=HEX ,1=Base64

**FileCRC24(String,Format)**

Returns CRC24 checksum of a File, Format 0=HEX ,1=Base64

**FileCRC32(String,Format)**

Returns CRC32 checksum of a File, Format 0=HEX ,1=Base64

**FileAdler32(String,Format)**

Returns Adler32 checksum of a File, Format 0=HEX ,1=Base64

**FileCRC64(String,Format)**

Returns CRC64 checksum of a File, Format 0=HEX ,1=Base64

**FileeDonkey(String,Format)
**
Returns eDonkey checksum of a File, Format 0=HEX ,1=Base64

**FileeMule(String,Format)**

Returns eMule checksum of a File, Format 0=HEX ,1=Base64

**FileMD4(String,Format)**

Returns MD4 checksum of a File, Format 0=HEX ,1=Base64

**FileMD5(String,Format)**

Returns MD5 checksum of a File, Format 0=HEX ,1=Base64

**FileRIPEMD160(String,Format)**

Returns RIPEMD160 checksum of a File, Format 0=HEX ,1=Base64

**FileSHA1(String,Format)**

Returns SHA1 checksum of a File, Format 0=HEX ,1=Base64

**FileSHA224(String,Format)**

Returns SHA224 checksum of a File, Format 0=HEX ,1=Base64

**FileSHA256(String,Format)**

Returns SHA256 checksum of a File, Format 0=HEX ,1=Base64

**FileSHA384(String,Format)**

Returns SHA384 checksum of a File, Format 0=HEX ,1=Base64

**FileSHA512(String,Format)**

Returns SHA512 checksum of a File, Format 0=HEX ,1=Base64

**FileWhirlpool(String,Format)**

Returns Whirlpool checksum of a File, Format 0=HEX ,1=Base64

## Date and Time Functions

**Day(Date,Format)**

Use Day to get the day part of a date value.

Day('01012003','DDMMYYYY')

**Hour(Date,Format)**

Use Hour to get the hour part of a date value.

Hour('01012003','DDMMYYYY')

**Minute(Date,Format)**

Use Minute to get the minute part of a date value.

Minute('01012003','DDMMYYYY')

**Month(Date,Format)**

Use Month to get the month part of a date value.

Month('01012003','DDMMYYYY')

**Second(Date,Format)**

Use Second to get the second part of a date value.

Second('01012003','DDMMYYYY')

**Year(Date,Format)**

Use Year to get the year part of a date value.

Year('01012003','DDMMYYYY')

**DayS(Date,Format)**

Use DayS to get the day part of a date value as string.

DayS('01012003','DDMMYYYY')

**HourS(Date,Format)**

Use HourS to get the hour part of a date value as string.

HourS('01012003','DDMMYYYY')

**MinuteS(Date,Format)**

Use MinuteS to get the minute part of a date value as string.

MinuteS('01012003','DDMMYYYY')

**MonthS(Date,Format)**

Use MonthS to get the month part of a date value as string.

MonthS('01012003','DDMMYYYY')

**SecondS(Date,Format)
**
Use SecondS to get the second part of a date value as string.

SecondS('01012003','DDMMYYYY')

**YearS(Date,Format)**

Use YearS to get the year part of a date value as string.

YearS('01012003','DDMMYYYY')

**IncDateS (Date,Format,ChangeType,Increment)**

ChangeType: YEAR,MONTH,WEEK,DAY,HOUR,MINUTE,SECOND

Use IncDateS to Increase ChangeType part of a date value by an Increment.

IncDateS ('01012003','DDMMYYYY', 'YEAR',1)

**DecDateS(Date,Format,ChangeType,Decrement)**

ChangeType: YEAR,MONTH,WEEK,DAY,HOUR,MINUTE,SECOND

Use DecDateS to Decrease ChangeType part of a date value by an Decrement.

DecDateS ('01012003','DDMMYYYY', 'YEAR',1)

**EncodeDate(Year,Month,Day)**

EncodeDate returns a TDateTime value from the values specified as the Year, Month, and Day parameters. The year must be between 1 and 9999. Valid Month values are 1 through 12. Valid Day values are 1 through 28, 29, 30, or 31, depending on the Month value. For example, the possible Day values for month 2 (February) are 1 through 28 or 1 through 29, depending on whether or not the Year value specifies a leap year.

**EncodeTime(Hour,Min,Sec,MSec)**

EncodeTime encodes the given hour, minute, second, and millisecond into a TDateTime value. Valid Hour values are 0 through 23. Valid Min and Sec values are 0 through 59. Valid MSec values are 0 through 999. If the specified values are not within range, EncodeTime raises an EConvertError exception. The resulting value is a number between 0 and 1 (inclusive) that indicates the fractional part of a day given by the specified time or (if 1.0) midnight on the following day. The value 0 corresponds to midnight, 0.5 corresponds to noon, 0.75 corresponds to 6:00 pm, and so on.

**DayOfWeek(D)**

DayOfWeek returns the day of the week of the specified date as an integer between 1 and 7, where Sunday is the first day of the week and Saturday is the seventh.

**Date**

Use Date to obtain the current local date as a TDateTime value. The time portion of the value is 0 (midnight).

**Time**

Use Time to return the current time as a TDateTime value. The two functions are completely equivalent.

**Now**

Returns the current date and time.

**IncMonth(D)**

IncMonth returns the value of the Date parameter, incremented by NumberOfMonths months. NumberOfMonths can be negative, to return a date N months previous. If the input day of month is greater than the last day of the resulting month, the day is set to the last day of the resulting month. The time of day specified by the Date parameter is copied to the result.

**IsLeapYear(D)**

Call IsLeapYear to determine whether the year specified by the Year parameter is a leap year. Year specifies the calendar year. Use YearOf to obtain the value of Year for IsLeapYear from a TDateTime value.

**DateToStr(D)**

Use DateToStr to obtain a string representation of a date value that can be used for display purposes.

**TimeToStr(D)**

TimeToStr converts the Time parameter, a TDateTime value, to a string.

**DateTimeToStr(D)**

Converts a TDateTime value to a string.

**StrToDate(S)**

Call StrToDate to parse a string that specifies a date. If S does not contain a valid date, StrToDate raises an exception.

**StrToTime(S)**

Call StrToTime to parse a string that specifies a time value. If S does not contain a valid time, StrToTime raises an exception.

**StrToDateTime(S)**

Call StrToDateTime to parse a string that specifies a date and time value. If S does not contain a valid date, StrToDateTime raises an exception.

**FormatDateTime(Format,DateTime)**

FormatDateTime formats the TDateTime value given by DateTime using the format given by Format. See the table below for information about the supported format strings.

**FormatStrToDate(String,Format)**

FormatStrToDate(String,Format):Date Converts String into date

**DateToEpoch(String,Format)**

DateToEpoch(String,Format):Integer Converts String into Epoch (Unix) Date

**EpochToDate(Integer)**

EpochToDate(Integer):Date Converts Epoch (Unix) Date into Date

**DateDiffS(Date1,Format1,Date2,Format2,ChangeType):String**

DateDiffS('20030101','YYYYMMDD','20000101','YYYYMMDD','YEAR')

Possible Change Type values are YEAR,MONTH,MONTH_EXACT,WEEK,DAY,HOUR,MINUTE,SECOND

When parameter is MONTH DateDiffS returns the approximate number of months between two specified Dates
The approximation based on an assumption of 30.4375 days per month.
To get exact number of months use MONTH_EXACT parameter

## Numeric Functions

**Round(Float,Integer)**

Use Round to round Value to a specified power of ten.
The following examples illustrate the use of Round:

| Expression        | Value   |
| ----------------- | ------- |
| Round(1234567, 3) | 1234000 |
| Round(1.234, -2)  | 1.23    |
| Round(1.235, -2)  | 1.24    |
| Round(1.245, -2)  | 1.24    |

**Sign(I)**

Use Sign to test the sign of a numeric value.
Sign returns
0 if AValue is zero.
1 if AValue is greater than zero.
-1 if AValue is less than zero.

**Abs(X)**

Returns an absolute value.

**Trunc(X)**

Truncates a real number to an integer.

**Ceil(X)**

Call Ceil to obtain the lowest integer greater than or equal to X. The absolute value of X must be less than MaxInt. For example: Ceil(-2.8) = -2 Ceil(2.8) = 3 Ceil(-1.0) = -1

**Floor(X)**

Call Floor to obtain the highest integer less than or equal to X. For example: Floor(-2.8) = -3 Floor(2.8) = 2 Floor(-1.0) = -1

**RandomRange(AFrom,ATo)**

RandomRange returns a random integer from the range that extends between AFrom and ATo (non-inclusive). RandomRange can handle negative ranges (where AFrom is greater than ATo). To initialize the random number generator, add a single call Randomize or assign a value to the RandSeed variable before making any calls to RandomRange.

**Max(A,B)**

Call Max to compare two numeric values. Max returns the greater value of the two.

**Min(A,B)**

Call Min to compare two numeric values in Delphi. Min returns the smaller value of the two.

## Miscellaneous Functions

**Iif(expr1=expr2;expr3;expr4)**

Iif function returns expr3 or expr4 depending on expr1=expr2

**GetSystemVariable(VariableName)**

GetSystemVariable returns value of 'VARIABLENAME'.

Possible values for 'VARIABLENAME' are:

- COMPUTERNAME
- OSUSERNAME
- DBUSERNAME
- BLOCKNUMBER
- LINENUMBER
- RECORDNUMBER
- SYSTEM_DATE
- SOURCE_FILE_NAME
- SOURCE_TABLE_NAME

**GetSystemDate(Format)**

Returns Current system date/time in format specified

GetSystemDate('MMDDYYYY')

**Pos(Substr,S)**

Pos searches for Substr within String and returns an integer value that is the index of the first character of Substr within String. Pos is case-sensitive. If Substr is not found, Pos returns zero.

**AnsiPos(Substr,S)**

Call AnsiPos to obtain the byte offset of the Substr parameter, as it appears in the string S. For example, if Substr is the string "AB", and S is the string "ABCDE", AnsiPos returns 1. If Substr does not appear in S, AnsiPos returns 0.

**Chr(X)**

Returns the character for a specified ASCII value.

**Length(X)**

Returns the number of characters in a string or elements in an array.

**Pos(Substr,Str)**

Pos searches for Substr within S and returns an integer value that is the index of the first character of Substr within S. Pos is case-sensitive. If Substr is not found, Pos returns zero

**SetLength(S,Length)
**
Set Length of dynamic array or string

**High(X)**

Call High to obtain the upper limit of an Array

**Low(X)**

Call Low to obtain the lowest value or first element of an Array.

**GetExcelCellValue(FileName,Sheet,Cell)**

Use GetExcelCellValue to Get Excel Cell Value for a specific file. This function will reduce performance.

**CommandLineParameter(ParameterNumber)**

Self-explanatory, 0 Returns executable name.

**ExecuteObject(ObjectID)**

Use ExecuteObject to execute object from the script inside the package

It returns the result of the package/transformation execution that was called.

- 0 = success
- 1 = failure

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/using-command-line-interface.png" title="ExecuteObject" >}}

## Procedures

**Abort**

Use Abort to escape from an execution path without reporting an error.

**Beep**

Beep generates a conventional message beep.

**Break**

The Break procedure forces a jump out of the set of statements within a loop

**Continue**

The Continue procedure forces a jump past the remaining statements within a loop, back to the next loop iteration

**Exit**

The Exit procedure abruptly terminates the current function or procedure.

**SourceChanged**

Forces data writer to create new file (Advanced ETL Processor only).

## Math functions

**Sqr(X)**

the Sqr function returns the square of the argument. X is a floating-point expression. The result, of the same type as X, is the square of X, or X\*X.

**Sqrt(X)**

The result is the square root of X.

**Exp(X)**

Exp returns the value of e raised to the power of X, where e is the base of the natural logarithms

**Ln(X)**

Ln returns the natural logarithm (Ln(e) = 1) of the real-type expression X.

**Sin(X)**

Sin returns the sine of the angle X in radians.

**Cos(X)**

Cos returns the cosine of the angle X. X expression that represents an angle in radians

**Tan(X)**

Tan returns the tangent of X. Tan(X) = Sin(X) / Cos(X).

**ArcTan(X)**

ArcTan returns the arctangent of X. X is a real-type expression that gives an angle in radians

**PI**

Represents the mathematical value pi, the ratio of a circle's circumference to its diameter. Pi is approximated as 3.1415926535897932385.

**ArcCos(X)**

ArcCos returns the inverse cosine of X. X must be between -1 and 1. The return value is in the range [0..Pi], in radians.

**ArcCosh(X)**

ArcCosh returns the inverse hyperbolic cosine of X. The value of X must be greater than or equal to 1.

**ArcCot(X)**

ArcCot returns the inverse cotangent of X.

**ArcCotH(X)**

ArcCot returns the inverse hyperbolic cotangent of X.

**ArcCsc(X)**

ArcCsc returns the inverse cosecant of X.

**ArcCscH(X)**

ArcCsc returns the inverse hyperbolic cosecant of X.

**ArcSec(X)**

ArcSec returns the inverse secant of X.

**ArcSecH(X)**

ArcSec returns the inverse hyperbolic secant of X.

**ArcSin(X)**

ArcSin returns the inverse sine of X. X must be between -1 and 1. The return value will be in the range [-Pi/2..Pi/2], in radians.

**ArcSinh(X)**

ArcSinh returns the inverse hyperbolic sine of X.

**ArcTan(X)**

ArcTan returns the arctangent of X. X is a real-type expression that gives an angle in radians.

**ArcTanh(X)**

ArcTanh returns the inverse hyperbolic tangent of X. The value of X must be between -1 and 1 (inclusive).

**Cosecant(X)**

Use the Cosecant to calculate the cosecant of X, where X is an angle in radians. The cosecant is calculated as 1/ Sin(X).

**Cosh(X)**

Use the Cosh to calculate the hyperbolic cosine of X.

**Cot(X)**

Call Cot to obtain the cotangent of X. The cotangent is calculated using the formula 1 / Tan (X).

**Cotan(X)**

Call Cotan to obtain the cotangent of X. The cotangent is calculated using the formula 1 / Tan (X)
Do not call Cotan with X = 0

**CotH(X)**

Call CotH to obtain the hyperbolic cotangent of X, where X is an angle in Radians.

**Csc(X)**

Use the Csc to calculate the cosecant of X, where X is an angle in radians.

**CscH(X)**

Use the CscH to calculate the hyperbolic cosecant of X, where X is an angle in radians.

**CycleToDeg(X)**

CycleToDeg converts angles measured in cycles into degrees, where degrees = cycles \* 360.

**CycleToGrad(X)**

CycleToGrad converts angles measured in cycles into grads.

**CycleToRad(X)**

CycleToRad converts angles measured in cycles into radians, where radians = 2pi \* cycles.

**DegToCycle(X)**

Use DegToCycle to convert angles expressed in degrees to the corresponding value in cycles.

**DegToGrad(X)**

Use DegToGrad to convert angles expressed in degrees to the corresponding value in grads.

**DegToRad(X)**

Use DegToRad to convert angles expressed in degrees to the corresponding value in radians, where radians = degrees(pi/180).

**GradToCycle(X)**

GradToCycle converts angles measured in grads into cycles.

**GradToDeg(X)**

GradToDeg converts angles measured in grads into degrees.

**GradToRad(X)**

GradToRad converts angles measured in grads into radians, where radians = grads(pi/200).

**Hypot(X,Y)**

Hypot returns the length of the hypotenuse of a right triangle. Specify the lengths of the sides adjacent to the right angle in X and Y. Hypot uses the formula Sqrt(X**2 + Y**2)

**IntPower(Base,Exponent)**

IntPower raises Base to the power specified by Exponent.

**Ldexp(X)**

Ldexp returns X times (2 to the power of P).

**LnXP1(X)**

LnXP1 returns the natural logarithm of (X+1). Use LnXP1 when X is a value near 0.

**Log10(X)**

Log10 returns the log base 10 of X.

**Log2(X)**

Log2 returns the log base 2 of X.

**LogN(Base,X)**

LogN returns the log base Base of X.

**Power(Base,Exponent)**

Power raises Base to any power. For fractional exponents or exponents greater than MaxInt, Base must be greater than 0.

**RadToCycle(X)**

Use RadToCycle to convert angles measured in radians into cycles, where cycles = radians/(2pi).

**RadToDeg(X)**

Use RadToDeg to convert angles measured in radians to degrees, where degrees = radians(180/pi).

**RadToGrad(X)**

Use RadToGrad to convert angles measured in radians to grads, where grads = radians(200/pi).

**RandG(Mean,StdDev)**

RandG produces random numbers with Gaussian distribution about the Mean. This is useful for simulating data with sampling errors and expected deviations from the Mean.

**Sec(X)**

Call Sec to obtain the secant of X, where X is an angle in radians. The secant is calculated using the formula 1 / Cos(X).

**SecH(X)**

Call SecH to obtain the hyperbolic secant of X, where X is an angle in Radians.

**Sinh(X)**

Sinh calculates the hyperbolic sine of X.

**Tan(X)**

Tan returns the tangent of X. Tan(X) = Sin(X) / Cos(X).

**Tanh(X)**

Tanh calculates the hyperbolic tangent of X.

## Useful Links

- [Scripting Language]({{<ref "scripting-language" >}})
- [Best practice for Calculations]({{<relref "/knowledgebase/tips/best-practice-for-calculations" >}})

{{< aetl >}}
