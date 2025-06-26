---
title: "Interface: PineJSStd | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd"
extracted_at: "2025-06-22T09:43:01.686Z"
---

- [](/charting-library-docs/)- Interfaces- PineJSStdOn this page# Interface: PineJSStd[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).PineJSStd

PineJS standard library functions.

## Properties[​](#properties)
### isZero[​](#iszero)
• isZero: (`v`: `number`) => `number`

Check if a value is zero.

#### Type declaration[​](#type-declaration)
▸ (`v`): `number`

Parameters[​](#parameters)
NameTypeDescription`v``number`the value to test.
Returns[​](#returns)
`number`

### max_series_default_size[​](#max_series_default_size)
• max_series_default_size: `10001`

Default maximum size of a pine series.

## Methods[​](#methods)
### abs[​](#abs)
▸ abs(`x`): `number`

Absolute value of x is x if x >= 0, or -x otherwise.

#### Parameters[​](#parameters-1)
NameType`x``number`
#### Returns[​](#returns-1)
`number`

The absolute value of `x`

### accdist[​](#accdist)
▸ accdist(`context`): `number`

Accumulation/distribution index.

#### Parameters[​](#parameters-2)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-2)
`number`

Accumulation/distribution index.

### acos[​](#acos)
▸ acos(`x`): `number`

The acos function returns the arccosine (in radians) of number such that `cos(acos(y)) = y` for `y` in range `[-1, 1]`.

#### Parameters[​](#parameters-3)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-3)
`number`

The arc cosine of a value; the returned angle is in the range `[0, Pi]`, or na if y is outside of range `[-1, 1]`.

### add_days_considering_dst[​](#add_days_considering_dst)
▸ add_days_considering_dst(`timezone`, `utcTime`, `daysCount`): `Date`

Get time in `daysCount` number of days while taking Daylight savings time into account.

#### Parameters[​](#parameters-4)
NameTypeDescription`timezone``string`Timezone`utcTime``Date`Date (JS built-in)`daysCount``number`Number of days
#### Returns[​](#returns-4)
`Date`

The time is `daysCount` number of days, taking into account Daylight savings time.

### add_years_considering_dst[​](#add_years_considering_dst)
▸ add_years_considering_dst(`timezone`, `utcTime`, `yearsCount`): `Date`

Get time in `yearsCount` number of years while taking Daylight savings time into account.

#### Parameters[​](#parameters-5)
NameTypeDescription`timezone``string`Timezone`utcTime``Date`Date (JS built-in)`yearsCount``number`Number of years
#### Returns[​](#returns-5)
`Date`

The time is `yearsCount` number of years, taking into account Daylight savings time.

### alma[​](#alma)
▸ alma(`series`, `length`, `offset`, `sigma`): `number`

Arnaud Legoux Moving Average. It uses Gaussian distribution as weights for moving average.

#### Parameters[​](#parameters-6)
NameTypeDescription`series`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`offset``number`Controls tradeoff between smoothness (closer to 1) and responsiveness (closer to 0).`sigma``number`Changes the smoothness of ALMA. The larger sigma the smoother ALMA.
#### Returns[​](#returns-6)
`number`

### and[​](#and)
▸ and(`n_0`, `n_1`): `number`

Logical AND.

#### Parameters[​](#parameters-7)
NameType`n_0``number``n_1``number`
#### Returns[​](#returns-7)
`number`

`1` if both values are truthy, `0` otherwise.

### asin[​](#asin)
▸ asin(`x`): `number`

The asin function returns the arcsine (in radians) of number such that `sin(asin(y)) = y` for `y` in range `[-1, 1]`.

#### Parameters[​](#parameters-8)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-8)
`number`

The arcsine of a value; the returned angle is in the range `[-Pi/2, Pi/2]`, or na if y is outside of range `[-1, 1]`.

### atan[​](#atan)
▸ atan(`x`): `number`

The atan function returns the arctangent (in radians) of number such that `tan(atan(y)) = y` for any `y`.

#### Parameters[​](#parameters-9)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-9)
`number`

The arc tangent of a value; the returned angle is in the range `[-Pi/2, Pi/2]`.

### atr[​](#atr)
▸ atr(`length`, `context`): `number`

Function atr (average true range) returns the RMA of true range. True range is `max(high - low, abs(high - close[1]), abs(low - close[1]))`

#### Parameters[​](#parameters-10)
NameTypeDescription`length``number`Length (number of bars back).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-10)
`number`

Average true range.

### avg[​](#avg)
▸ avg(`...values`): `number`

Calculates average of all given series (elementwise).

#### Parameters[​](#parameters-11)
NameType`...values``number`[]
#### Returns[​](#returns-11)
`number`

the average of the values

### ceil[​](#ceil)
▸ ceil(`x`): `number`

The ceil function returns the smallest (closest to negative infinity) integer that is greater than or equal to the argument.

#### Parameters[​](#parameters-12)
NameType`x``number`
#### Returns[​](#returns-12)
`number`

The smallest integer greater than or equal to the given number.

### change[​](#change)
▸ change(`source`): `number`

Difference between current value and previous, `x - x[1]`.

#### Parameters[​](#parameters-13)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series to process.
#### Returns[​](#returns-13)
`number`

The result of subtraction.

### close[​](#close)
▸ close(`context`): `number`

Close Price

#### Parameters[​](#parameters-14)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-14)
`number`

Current close price.

### compare[​](#compare)
▸ compare(`n1`, `n2`, `eps?`): `-1` | `0` | `1`

Compare the values of `n1` and `n2`

#### Parameters[​](#parameters-15)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-15)
`-1` | `0` | `1`

`0` if values are equal. `1` if x1 is greater than x2. `-1` if x1 is less than x2

### correlation[​](#correlation)
▸ correlation(`sourceA`, `sourceB`, `length`, `context`): `number`

Correlation coefficient. Describes the degree to which two series tend to deviate from their `sma` values.

#### Parameters[​](#parameters-16)
NameTypeDescription`sourceA`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Source series.`sourceB`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Target series.`length``number`Length (number of bars back).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-16)
`number`

Correlation coefficient.

### cos[​](#cos)
▸ cos(`x`): `number`

The cos function returns the trigonometric cosine of an angle.

#### Parameters[​](#parameters-17)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-17)
`number`

The trigonometric cosine of an angle.

### createNewSessionCheck[​](#createnewsessioncheck)
▸ createNewSessionCheck(`context`): (`time`: `number`) => `boolean`

checks whether a new session can be created

#### Parameters[​](#parameters-18)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-18)
`fn`

checks whether a new session can be created

▸ (`time`): `boolean`

Parameters[​](#parameters-19)
NameType`time``number`
Returns[​](#returns-19)
`boolean`

### cross[​](#cross)
▸ cross(`n_0`, `n_1`, `context`): `boolean`

Crossing of series.

#### Parameters[​](#parameters-20)
NameTypeDescription`n_0``number`First value.`n_1``number`Second value.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-20)
`boolean`

`true` if two series have crossed each other, otherwise `false`.

### cum[​](#cum)
▸ cum(`n_value`, `context`): `number`

Cumulative (total) sum. The function tracks the previous values internally.

#### Parameters[​](#parameters-21)
NameTypeDescription`n_value``number`Value to add to the sum.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-21)
`number`

The sum.

### currencyCode[​](#currencycode)
▸ currencyCode(`ctx`): `string`

Get the symbol currency code.

#### Parameters[​](#parameters-22)
NameTypeDescription`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-22)
`string`

Symbol currency code.

### dayofmonth[​](#dayofmonth)
▸ dayofmonth(`context`, `time?`): `number`

Day of month for current bar time in exchange timezone.

#### Parameters[​](#parameters-23)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-23)
`number`

Day of month for current bar time in exchange timezone.

### dayofweek[​](#dayofweek)
▸ dayofweek(`context`, `time?`): `number`

Day of week for current bar time in exchange timezone.

#### Parameters[​](#parameters-24)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-24)
`number`

Day of week for current bar time in exchange timezone.

### dev[​](#dev)
▸ dev(`source`, `length`, `context`): `number`

Measure of difference between the series and its sma.

#### Parameters[​](#parameters-25)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-25)
`number`

Deviation of source for length bars back.

### dmi[​](#dmi)
▸ dmi(`diLength`, `adxSmoothingLength`, `context`): [`number`, `number`, `number`, `number`, `number`]

Calculates the directional movement values +DI, -DI, DX, ADX, and ADXR.

#### Parameters[​](#parameters-26)
NameTypeDescription`diLength``number`Number of bars (length) used when calculating the +DI and -DI values.`adxSmoothingLength``number`Number of bars (length) used when calculating the ADX value.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-26)
[`number`, `number`, `number`, `number`, `number`]

An array of the +DI, -DI, DX, ADX, and ADXR values with diLength smoothing for the (+/-)DI values and adxSmoothingLength for the ADX value.

### ema[​](#ema)
▸ ema(`source`, `length`, `context`): `number`

Exponential Moving Average. In EMA weighting factors decrease exponentially.

It calculates by using a formula: `EMA = alpha * x + (1 - alpha) * EMA[1]`, where `alpha = 2 / (y + 1)`.

#### Parameters[​](#parameters-27)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-27)
`number`

Exponential moving average of `x` with `alpha = 2 / (y + 1)`

### eps[​](#eps)
▸ eps(): `number`

Epsilon (machine precision)

#### Returns[​](#returns-28)
`number`

Epsilon (machine precision). Upper bound on the relative approximation error due to rounding in floating point arithmetic.

### eq[​](#eq)
▸ eq(`n1`, `n2`): `number`

Checks if `n1` is equal to `n2`.

#### Parameters[​](#parameters-28)
NameType`n1``number``n2``number`
#### Returns[​](#returns-29)
`number`

`1` if `n1` is equal to `n2`, `0` otherwise.

### equal[​](#equal)
▸ equal(`n1`, `n2`, `eps?`): `boolean`

Checks if `n1` is equal to `n2` (within the accuracy of epsilon).

#### Parameters[​](#parameters-29)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-30)
`boolean`

True if `n1` is equal to `n2`.

### error[​](#error)
▸ error(`message`): `never`

Display an error message.

#### Parameters[​](#parameters-30)
NameTypeDescription`message``string`message to display for error
#### Returns[​](#returns-31)
`never`

### exp[​](#exp)
▸ exp(`x`): `number`

The exp function of `x` is `e^x`, where `x` is the argument and `e` is Euler's number.

#### Parameters[​](#parameters-31)
NameType`x``number`
#### Returns[​](#returns-32)
`number`

A number representing `e^x`.

### falling[​](#falling)
▸ falling(`series`, `length`): `number`

Test if the series is now falling for length bars long.

#### Parameters[​](#parameters-32)
NameTypeDescription`series`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).
#### Returns[​](#returns-33)
`number`

`true` if current `x` is less than any previous `x` for length bars back, `false` otherwise.

### fixnan[​](#fixnan)
▸ fixnan(`n_current`, `context`): `number`

For a given series replaces NaN values with previous nearest non-NaN value.

#### Parameters[​](#parameters-33)
NameTypeDescription`n_current``number`Series of values to process.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-34)
`number`

Series without na gaps.

### floor[​](#floor)
▸ floor(`x`): `number`

Round the number down to the closest integer

#### Parameters[​](#parameters-34)
NameType`x``number`
#### Returns[​](#returns-35)
`number`

The largest integer less than or equal to the given number.

### ge[​](#ge)
▸ ge(`n1`, `n2`): `number`

Checks if `n1` is greater than or equal to `n2`

#### Parameters[​](#parameters-35)
NameType`n1``number``n2``number`
#### Returns[​](#returns-36)
`number`

`1` if `n1` is greater than or equal to `n2`, `0` otherwise.

### greater[​](#greater)
▸ greater(`n1`, `n2`, `eps?`): `boolean`

Checks if `n1` is greater than `n2`

#### Parameters[​](#parameters-36)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-37)
`boolean`

True if `n1` is greater than `n2`.

### greaterOrEqual[​](#greaterorequal)
▸ greaterOrEqual(`n1`, `n2`, `eps?`): `boolean`

Checks if `n1` is greater than or equal to `n2`

#### Parameters[​](#parameters-37)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-38)
`boolean`

True if `n1` is greater than or equal to `n2`.

### gt[​](#gt)
▸ gt(`n1`, `n2`): `number`

Checks if `n1` is greater than `n2`

#### Parameters[​](#parameters-38)
NameType`n1``number``n2``number`
#### Returns[​](#returns-39)
`number`

`1` if `n1` is greater than `n2`, `0` otherwise.

### high[​](#high)
▸ high(`context`): `number`

High Price

#### Parameters[​](#parameters-39)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-40)
`number`

Current high price.

### highest[​](#highest)
▸ highest(`source`, `length`, `context`): `number`

Highest value for a given number of bars back.

#### Parameters[​](#parameters-40)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-41)
`number`

Highest value.

### highestbars[​](#highestbars)
▸ highestbars(`source`, `length`, `context`): `number`

Highest value offset for a given number of bars back.

#### Parameters[​](#parameters-41)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-42)
`number`

Offset to the highest bar.

### hl2[​](#hl2)
▸ hl2(`context`): `number`

Is a shortcut for (high + low)/2

#### Parameters[​](#parameters-42)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-43)
`number`

Calculated average of the current HL values

### hlc3[​](#hlc3)
▸ hlc3(`context`): `number`

Is a shortcut for (high + low + close)/3

#### Parameters[​](#parameters-43)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-44)
`number`

Calculated average of the current HLC values

### hour[​](#hour)
▸ hour(`context`, `time?`): `number`

Hour of current bar time in exchange timezone.

#### Parameters[​](#parameters-44)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-45)
`number`

Current bar hour in exchange timezone.

### iff[​](#iff)
▸ iff(`condition`, `thenValue`, `elseValue`): `number`

If ... then ... else ...
`iff` does exactly the same thing as ternary conditional operator `?:` but in a functional style. Also `iff` is slightly less efficient than operator `?:`
#### Parameters[​](#parameters-45)
NameTypeDescription`condition``number`condition to check`thenValue``number`value to use if condition is true`elseValue``number`value to use if condition is false
#### Returns[​](#returns-46)
`number`

either thenValue or elseValue

### interval[​](#interval)
▸ interval(`ctx`): `number`

Get the symbol interval. For example: if the symbol has a resolution of `1D` then this function would return `1`.

#### Parameters[​](#parameters-46)
NameTypeDescription`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-47)
`number`

Symbol interval.

### isdaily[​](#isdaily)
▸ isdaily(`context`): `boolean`

Determines whether the current resolution is a daily resolution.

#### Parameters[​](#parameters-47)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-48)
`boolean`

true if current resolution is a daily resolution

### isdwm[​](#isdwm)
▸ isdwm(`context`): `boolean`

Determines whether the current resolution is a daily, weekly, or monthly resolution.

#### Parameters[​](#parameters-48)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-49)
`boolean`

true if current resolution is a daily or weekly or monthly resolution

### isintraday[​](#isintraday)
▸ isintraday(`context`): `boolean`

Determines whether the current resolution is an intraday (minutes or seconds) resolution.

#### Parameters[​](#parameters-49)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-50)
`boolean`

true if current resolution is an intraday (minutes or seconds) resolution

### ismonthly[​](#ismonthly)
▸ ismonthly(`context`): `boolean`

Determines whether the current resolution is a monthly resolution.

#### Parameters[​](#parameters-50)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-51)
`boolean`

true if current resolution is a monthly resolution

### isweekly[​](#isweekly)
▸ isweekly(`context`): `boolean`

Determines whether the current resolution is a weekly resolution.

#### Parameters[​](#parameters-51)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-52)
`boolean`

true if current resolution is a weekly resolution

### le[​](#le)
▸ le(`n1`, `n2`): `number`

Checks if `n1` is less than or equal to `n2`

#### Parameters[​](#parameters-52)
NameType`n1``number``n2``number`
#### Returns[​](#returns-53)
`number`

`1` if `n1` is greater than or equal to `n2`, `0` otherwise.

### less[​](#less)
▸ less(`n1`, `n2`, `eps?`): `boolean`

Checks if `n1` is less than `n2`

#### Parameters[​](#parameters-53)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-54)
`boolean`

True if `n1` is less than `n2`.

### lessOrEqual[​](#lessorequal)
▸ lessOrEqual(`n1`, `n2`, `eps?`): `boolean`

Checks if `n1` is less than or equal to `n2`

#### Parameters[​](#parameters-54)
NameTypeDescription`n1``number``n2``number``eps?``number`Epsilon (Optional).
#### Returns[​](#returns-55)
`boolean`

True if `n1` is less than or equal to `n2`.

### linreg[​](#linreg)
▸ linreg(`source`, `length`, `offset`): `number`

Linear regression curve. A line that best fits the prices specified over a user-defined time period.
It is calculated using the least squares method. The result of this function is calculated using the formula:
`linreg = intercept + slope * (length - 1 - offset)`, where intercept and slope are the values calculated with
the least squares method on source series (x argument).
#### Parameters[​](#parameters-55)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Source series.`length``number`Length (number of bars back).`offset``number`Offset (number of bars)
#### Returns[​](#returns-56)
`number`

Linear regression curve point.

### log[​](#log)
▸ log(`x`): `number`

Natural logarithm of any `x > 0` is the unique `y` such that `e^y = x`

#### Parameters[​](#parameters-56)
NameType`x``number`
#### Returns[​](#returns-57)
`number`

The natural logarithm of `x`.

### log10[​](#log10)
▸ log10(`x`): `number`

Base 10 logarithm of any `x > 0` is the unique `y` such that `10^y = x`

#### Parameters[​](#parameters-57)
NameType`x``number`
#### Returns[​](#returns-58)
`number`

The base 10 logarithm of `x`.

### low[​](#low)
▸ low(`context`): `number`

Low Price

#### Parameters[​](#parameters-58)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-59)
`number`

Current low price.

### lowest[​](#lowest)
▸ lowest(`source`, `length`, `context`): `number`

Lowest value for a given number of bars back.

#### Parameters[​](#parameters-59)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-60)
`number`

Lowest value.

### lowestbars[​](#lowestbars)
▸ lowestbars(`source`, `length`, `context`): `number`

Lowest value offset for a given number of bars back.

#### Parameters[​](#parameters-60)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-61)
`number`

Offset to the lowest bar.

### lt[​](#lt)
▸ lt(`n1`, `n2`): `number`

Checks if `n1` is less than `n2`

#### Parameters[​](#parameters-61)
NameType`n1``number``n2``number`
#### Returns[​](#returns-62)
`number`

`1` if `n1` is less than `n2`, `0` otherwise.

### max[​](#max)
▸ max(`...values`): `number`

Maximum number in the array

#### Parameters[​](#parameters-62)
NameType`...values``number`[]
#### Returns[​](#returns-63)
`number`

The greatest of multiple given values

### min[​](#min)
▸ min(`...values`): `number`

Minimum number in the array

#### Parameters[​](#parameters-63)
NameType`...values``number`[]
#### Returns[​](#returns-64)
`number`

The smallest of multiple given values

### minute[​](#minute)
▸ minute(`context`, `time?`): `number`

Minute of current bar time in exchange timezone.

#### Parameters[​](#parameters-64)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-65)
`number`

Current bar minute in exchange timezone.

### month[​](#month)
▸ month(`context`, `time?`): `number`

Month of current bar time in exchange timezone.

#### Parameters[​](#parameters-65)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-66)
`number`

Current bar month in exchange timezone.

### n[​](#n)
▸ n(`context`): `number`

Current bar index

#### Parameters[​](#parameters-66)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-67)
`number`

Current bar index. Numbering is zero-based, index of the first historical bar is 0.

### na[​](#na)
▸ na(`n?`): `number`

Test value if it's a NaN.

#### Parameters[​](#parameters-67)
NameTypeDescription`n?``number`value to test
#### Returns[​](#returns-68)
`number`

`1` if `n` is not a valid number (`n` is `NaN`), otherwise `0`. Returns `NaN` if `n` is undefined.

### neq[​](#neq)
▸ neq(`n1`, `n2`): `number`

Checks if `n1` is not equal to `n2`.

#### Parameters[​](#parameters-68)
NameType`n1``number``n2``number`
#### Returns[​](#returns-69)
`number`

`1` if `n1` is not equal to `n2`, `0` otherwise.

### not[​](#not)
▸ not(`n_0`): `number`

Logical negation (NOT).

#### Parameters[​](#parameters-69)
NameType`n_0``number`
#### Returns[​](#returns-70)
`number`

`1` if value is falsy, `0` if value is truthy.

### nz[​](#nz)
▸ nz(`x`, `y?`): `number`

Replaces NaN values with zeros (or given value) in a series.

#### Parameters[​](#parameters-70)
NameTypeDescription`x``number`value to test (and potentially replace)`y?``number`fallback value. `0` by default.
#### Returns[​](#returns-71)
`number`

`x` if it's a valid (not NaN) number, otherwise `y`

### ohlc4[​](#ohlc4)
▸ ohlc4(`context`): `number`

Is a shortcut for (open + high + low + close)/4

#### Parameters[​](#parameters-71)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-72)
`number`

Calculated average of the current OHLC values

### open[​](#open)
▸ open(`context`): `number`

Open Price

#### Parameters[​](#parameters-72)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-73)
`number`

Current open price.

### or[​](#or)
▸ or(`n_0`, `n_1`): `number`

Logical OR.

#### Parameters[​](#parameters-73)
NameType`n_0``number``n_1``number`
#### Returns[​](#returns-74)
`number`

`1` if either value is truthy, `0` otherwise.

### percentrank[​](#percentrank)
▸ percentrank(`source`, `length`): `number`

Percent rank is the percentage of how many previous values were less than or equal to the current value of given series.

#### Parameters[​](#parameters-74)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).
#### Returns[​](#returns-75)
`number`

Percent rank of `source` for `length` bars back.

### period[​](#period)
▸ period(`context`): `string`

Resolution string, e.g. 60 - 60 minutes, D - daily, W - weekly, M - monthly, 5D - 5 days, 12M - one year, 3M - one quarter

#### Parameters[​](#parameters-75)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-76)
`string`

The resolution string for the current context

### pow[​](#pow)
▸ pow(`base`, `exponent`): `number`

Mathematical power function.

#### Parameters[​](#parameters-76)
NameTypeDescription`base``number`Specify the base to use.`exponent``number`Specifies the exponent.
#### Returns[​](#returns-77)
`number`

`x` raised to the power of `y`.

### rising[​](#rising)
▸ rising(`series`, `length`): `number`

Test if the series is now rising for length bars long.

#### Parameters[​](#parameters-77)
NameTypeDescription`series`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).
#### Returns[​](#returns-78)
`number`

`true` if current `x` is greater than any previous `x` for length bars back, `false` otherwise.

### rma[​](#rma)
▸ rma(`source`, `length`, `context`): `number`

Moving average used in RSI. It is the exponentially weighted moving average with `alpha = 1 / length`.

#### Parameters[​](#parameters-78)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-79)
`number`

Exponential moving average of `x` with `alpha = 1 / y`.

### roc[​](#roc)
▸ roc(`source`, `length`): `number`

Rate of Change.

Function roc (rate of change) showing the difference between current value of `source` and the value of `source` that was `length` days ago. It is calculated by the formula: `100 * change(src, length) / src[length]`.

#### Parameters[​](#parameters-79)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).
#### Returns[​](#returns-80)
`number`

The rate of change of `source` for `length` bars back.

### round[​](#round)
▸ round(`x`): `number`

Round the number to the nearest integer

#### Parameters[​](#parameters-80)
NameType`x``number`
#### Returns[​](#returns-81)
`number`

The value of `x` rounded to the nearest integer, with ties rounding up. If the precision parameter is used, returns a float value rounded to that number of decimal places.

### rsi[​](#rsi)
▸ rsi(`upper`, `lower`): `number`

Relative strength index. It is calculated based on rma's of upward and downward change of x.

#### Parameters[​](#parameters-81)
NameTypeDescription`upper``number`upward change`lower``number`downward change
#### Returns[​](#returns-82)
`number`

Relative strength index.

### sar[​](#sar)
▸ sar(`start`, `inc`, `max`, `context`): `number`

Parabolic SAR (parabolic stop and reverse) is a method devised by J. Welles Wilder, Jr., to find potential reversals in the market price direction of traded goods.

#### Parameters[​](#parameters-82)
NameTypeDescription`start``number`Start.`inc``number`Increment.`max``number`Maximum.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-83)
`number`

Parabolic SAR value.

### second[​](#second)
▸ second(`context`, `time?`): `number`

Second of current bar time in exchange timezone.

#### Parameters[​](#parameters-83)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-84)
`number`

Current bar second in exchange timezone.

### selectSessionBreaks[​](#selectsessionbreaks)
▸ selectSessionBreaks(`context`, `times`): `number`[]

select session breaks for intraday resolutions only

#### Parameters[​](#parameters-84)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`times``number`[]An array of numbers representing the times to select session breaks from.
#### Returns[​](#returns-85)
`number`[]

session breaks for intraday resolutions only.

### sign[​](#sign)
▸ sign(`x`): `number`

Sign (signum) of `x` is `0` if the x is zero, `1.0` if the `x` is greater than zero, `-1.0` if the `x` is less than zero.

#### Parameters[​](#parameters-85)
NameType`x``number`
#### Returns[​](#returns-86)
`number`

The sign of `x`

### sin[​](#sin)
▸ sin(`x`): `number`

The sin function returns the trigonometric sine of an angle.

#### Parameters[​](#parameters-86)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-87)
`number`

The trigonometric sine of an angle.

### sma[​](#sma)
▸ sma(`source`, `length`, `context`): `number`

Simple Moving Average. The sum of last `length` values of `source`, divided by `length`.

#### Parameters[​](#parameters-87)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-88)
`number`

Simple moving average of x for y bars back.

### smma[​](#smma)
▸ smma(`n_value`, `n_length`, `ctx`): `number`

Smoothed Moving Average.

#### Parameters[​](#parameters-88)
NameTypeDescription`n_value``number`Next value in the series to calculate.`n_length``number`Smoothing length.`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-89)
`number`

The smoothed moving average value.

### sqrt[​](#sqrt)
▸ sqrt(`x`): `number`

Square root of any `x >= 0` is the unique `y >= 0` such that `y^2 = x`

#### Parameters[​](#parameters-89)
NameType`x``number`
#### Returns[​](#returns-90)
`number`

The square root of `x`

### stdev[​](#stdev)
▸ stdev(`source`, `length`, `context`): `number`

Standard deviation. Note: This is a biased estimation of standard deviation.

#### Parameters[​](#parameters-90)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-91)
`number`

Standard deviation.

### stoch[​](#stoch)
▸ stoch(`source`, `high`, `low`, `length`, `context`): `number`

Stochastic. It is calculated by a formula: `100 * (close - lowest(low, length)) / (highest(high, length) - lowest(low, length))`

#### Parameters[​](#parameters-91)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Source series.`high`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of high.`low`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of low.`length``number`Length (number of bars back).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-92)
`number`

Stochastic value.

### sum[​](#sum)
▸ sum(`source`, `length`, `context`): `number`

The sum function returns the sliding sum of last y values of x.

#### Parameters[​](#parameters-92)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-93)
`number`

Sum of x for y bars back.

### swma[​](#swma)
▸ swma(`source`, `context`): `number`

Symmetrically weighted moving average with fixed length: 4. Weights: `[1/6, 2/6, 2/6, 1/6]`.

#### Parameters[​](#parameters-93)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-94)
`number`

Symmetrically weighted moving average

### tan[​](#tan)
▸ tan(`x`): `number`

The tan function returns the trigonometric tangent of an angle.

#### Parameters[​](#parameters-94)
NameTypeDescription`x``number`Angle, in radians.
#### Returns[​](#returns-95)
`number`

The trigonometric tangent of an angle.

### ticker[​](#ticker)
▸ ticker(`context`): `string`

Ticker ID for the current symbol

#### Parameters[​](#parameters-95)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-96)
`string`

Ticker ID for the current symbol

### tickerid[​](#tickerid)
▸ tickerid(`context`): `string`

Ticker ID

#### Parameters[​](#parameters-96)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-97)
`string`

Ticker ID for the current symbol

### time[​](#time)
▸ time(`context`): `number`

Current bar time

#### Parameters[​](#parameters-97)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-98)
`number`

UNIX time of current bar according to the symbol timezone and not UTC.

▸ time(`context`, `period`): `number`

Current bar time

#### Parameters[​](#parameters-98)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`period``string`Period
#### Returns[​](#returns-99)
`number`

UNIX time of current bar according to the symbol timezone and not UTC.

### toBool[​](#tobool)
▸ toBool(`v`): `boolean`

Convert a number to a boolean.

#### Parameters[​](#parameters-99)
NameTypeDescription`v``number`the value to convert.
#### Returns[​](#returns-100)
`boolean`

`true` if the number is finite and non-zero, `false` otherwise.

### tr[​](#tr)
▸ tr(`n_handleNaN`, `ctx`): `number`

True Range

#### Parameters[​](#parameters-100)
NameTypeDescription`n_handleNaN``number`How NaN values are handled. If truthy, and previous bar's close is `NaN` then tr would be calculated as current bar `high-low`. Otherwise tr would return `NaN` in such cases. Also note, that `atr` uses `tr(true)`.`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-101)
`number`

True range. It is `max(high - low, abs(high - close[1]), abs(low - close[1]))`

### tsi[​](#tsi)
▸ tsi(`source`, `shortLength`, `longLength`, `context`): `number`

True strength index. It uses moving averages of the underlying momentum of a financial instrument.

#### Parameters[​](#parameters-101)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Source series.`shortLength``number`Length (number of bars back).`longLength``number`Length (number of bars back).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-102)
`number`

True strength index. A value in range `[-1, 1]`

### unitId[​](#unitid)
▸ unitId(`ctx`): `string`

Get the symbol unit ID.

#### Parameters[​](#parameters-102)
NameTypeDescription`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-103)
`string`

Symbol unit ID.

### updatetime[​](#updatetime)
▸ updatetime(`context`): `number`

Time of the current update

#### Parameters[​](#parameters-103)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-104)
`number`

symbol update time

### variance[​](#variance)
▸ variance(`source`, `length`, `context`): `number`

Variance is the expectation of the squared deviation of a series from its mean `sma`, and it informally measures how far a set of numbers are spread out from their mean. Note: This is a biased estimation of sample variance.

#### Parameters[​](#parameters-104)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-105)
`number`

Variance of `source` for `length` bars back.

### volume[​](#volume)
▸ volume(`context`): `number`

Current bar volume

#### Parameters[​](#parameters-105)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-106)
`number`

Current bar volume

### vwma[​](#vwma)
▸ vwma(`source`, `length`, `context`): `number`

The vwma function returns volume-weighted moving average of `source` for `length` bars back. It is the same as: `sma(x * volume, y) / sma(volume, y)`

#### Parameters[​](#parameters-106)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-107)
`number`

Volume-weighted moving average of `source` for `length` bars back.

### weekofyear[​](#weekofyear)
▸ weekofyear(`context`, `time?`): `number`

Week number of current bar time in exchange timezone.

#### Parameters[​](#parameters-107)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-108)
`number`

Week number of current bar in exchange timezone.

### wma[​](#wma)
▸ wma(`source`, `length`, `context`): `number`

The wma function returns weighted moving average of `source` for `length` bars back. In wma weighting factors decrease in arithmetical progression.

#### Parameters[​](#parameters-108)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Series of values to process.`length``number`Number of bars (length).`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-109)
`number`

Weighted moving average of `series` for `length` bars back.

### year[​](#year)
▸ year(`context`, `time?`): `number`

Year of current bar time in exchange timezone.

#### Parameters[​](#parameters-109)
NameTypeDescription`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.`time?``number`optional time. Current bar time will be used by default.
#### Returns[​](#returns-110)
`number`

Current bar year in exchange timezone.

### zigzag[​](#zigzag)
▸ zigzag(`n_deviation`, `n_depth`, `context`): `number`

Zig-zag pivot points

#### Parameters[​](#parameters-110)
NameTypeDescription`n_deviation``number`Deviation`n_depth``number`Depth (integer)`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-111)
`number`

the zig-zag pivot points

### zigzagbars[​](#zigzagbars)
▸ zigzagbars(`n_deviation`, `n_depth`, `context`): `number`

Zig-zag pivot points

#### Parameters[​](#parameters-111)
NameTypeDescription`n_deviation``number`Deviation`n_depth``number`Depth (integer)`context`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)PineJS execution context.
#### Returns[​](#returns-112)
`number`

the zig-zag pivot points (for bars)

- [Properties](#properties)[isZero](#iszero)- [max_series_default_size](#max_series_default_size)- [Methods](#methods)[abs](#abs)- [accdist](#accdist)- [acos](#acos)- [add_days_considering_dst](#add_days_considering_dst)- [add_years_considering_dst](#add_years_considering_dst)- [alma](#alma)- [and](#and)- [asin](#asin)- [atan](#atan)- [atr](#atr)- [avg](#avg)- [ceil](#ceil)- [change](#change)- [close](#close)- [compare](#compare)- [correlation](#correlation)- [cos](#cos)- [createNewSessionCheck](#createnewsessioncheck)- [cross](#cross)- [cum](#cum)- [currencyCode](#currencycode)- [dayofmonth](#dayofmonth)- [dayofweek](#dayofweek)- [dev](#dev)- [dmi](#dmi)- [ema](#ema)- [eps](#eps)- [eq](#eq)- [equal](#equal)- [error](#error)- [exp](#exp)- [falling](#falling)- [fixnan](#fixnan)- [floor](#floor)- [ge](#ge)- [greater](#greater)- [greaterOrEqual](#greaterorequal)- [gt](#gt)- [high](#high)- [highest](#highest)- [highestbars](#highestbars)- [hl2](#hl2)- [hlc3](#hlc3)- [hour](#hour)- [iff](#iff)- [interval](#interval)- [isdaily](#isdaily)- [isdwm](#isdwm)- [isintraday](#isintraday)- [ismonthly](#ismonthly)- [isweekly](#isweekly)- [le](#le)- [less](#less)- [lessOrEqual](#lessorequal)- [linreg](#linreg)- [log](#log)- [log10](#log10)- [low](#low)- [lowest](#lowest)- [lowestbars](#lowestbars)- [lt](#lt)- [max](#max)- [min](#min)- [minute](#minute)- [month](#month)- [n](#n)- [na](#na)- [neq](#neq)- [not](#not)- [nz](#nz)- [ohlc4](#ohlc4)- [open](#open)- [or](#or)- [percentrank](#percentrank)- [period](#period)- [pow](#pow)- [rising](#rising)- [rma](#rma)- [roc](#roc)- [round](#round)- [rsi](#rsi)- [sar](#sar)- [second](#second)- [selectSessionBreaks](#selectsessionbreaks)- [sign](#sign)- [sin](#sin)- [sma](#sma)- [smma](#smma)- [sqrt](#sqrt)- [stdev](#stdev)- [stoch](#stoch)- [sum](#sum)- [swma](#swma)- [tan](#tan)- [ticker](#ticker)- [tickerid](#tickerid)- [time](#time)- [toBool](#tobool)- [tr](#tr)- [tsi](#tsi)- [unitId](#unitid)- [updatetime](#updatetime)- [variance](#variance)- [volume](#volume)- [vwma](#vwma)- [weekofyear](#weekofyear)- [wma](#wma)- [year](#year)- [zigzag](#zigzag)- [zigzagbars](#zigzagbars)