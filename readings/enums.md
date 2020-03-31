# Enums

## What Are Enums?

An _enumeration type_ (or **_enum_**) is defined by a set of named constants (words / strings) that represent an integer type (whole numbers).

## Enum Index Values

By default, the integer value of an enum constant starts at `0` and increases sequentially for each constant. This number can be altered or set manually. If this is done, then the remaining numbers continue sequentially from the manually input value unless modified again.

## Example

An example of that would look like so:
```
enum MonthsInAYear
{
    January, // Value = 0
    February, // Value = 1
    March, // Value = 2
    April = 5, // Value = 5
    May, // Value = 6
    June, // Value = 7
    July, // Value = 8
    August, // Value = 9
    September = 22, // Value = 22
    October, // Value = 23
    November, // Value = 24
    December // Value = 25
}
```

## Conversions

You can convert an enum type to its integer value. If you cast an enum's explicit constant to the integer value, the integer value is returned, and vice-versa.
