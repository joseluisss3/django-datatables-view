## 2022.04.05 - 1.20.0
 - Switched to MIT license
 - Minimum required version of Django is now 3.0
 - Changed project structure (added src/ subdirectory)
 - Updated setuptools configurations
 - Django 4.0 compatibility
 - Code formatting
 - Issue #84 - fixed force_url
 - Issue #87 - updated Readme
 - Issue #85 - added count_records method

## 2019.11.20 - 1.19.1
 - Issue #63 - render_column method refactored into two separate methods
 - Issue #66 - added format_html to the render_column output if get_absolute_url is used

## 2019.10.02 - 1.19.0
 - Fixed backward compatibility with version 1.16
 - Use columns.data field (if defined in JavaScript) to determine columns definition

## 2019.06.09 - 1.18.0
 - Added support for dict (.values) to rendering method (thanks Andreas Hasenkopf)

## 2018.09.04 - 1.17.0
 - If 'name' field is defined in columns definition (JS side) then it can be used to create 'columns' and
   'order_columns' (see django-datatables-view-example for sample code).
 - Added get_filter_method method to make it possible to easily change filter from istartswith to e.g. icontains.

## 2018.04.17 - 1.16.0
 - removed exception handling - let exceptions propagate in a normal django flow (backward incompatible change!)
   Previously django_datatables_view has handled exceptions and returned these to datatables as JSON with status code
   200. This caused that exceptions might have been not properly recorded eg. by Sentry.

## 2018.03.05 - 1.15.1
 - added handle_exception method in order to make exception handling easier. Thanks pmourlanne.

## 2018.03.04 - 1.15.0
 - possible backward incomatible change: escape() is now called for each value returned by render_column.
   This can be disabled by setting class attribute: escape_values to False.

## 2017.02.01 - 1.14.0
 - render_column method is now able to call get_OBJECT_display on foreign models (issue #31)
 - potentially backward incompatible change in render_column - get_absolute_url is now called on obj that is
   computed from dotted notation

## 2016.10.30 - 1.13.2
 - Make POST requests work (thanks Adam Taylor)
 - Change handling of 'result' error/ok state by JSONResponseMixin (Issue #26)

## 2016.07.14 - 1.13.1
 - updated Trove classifiers in setup.py (issue #25)

## 2015.11.08 - 1.13.0
 - handle foreign keys while filtering - thanks Bruno Lottero
 - added none_string property - thanks Alan Moore

## 2015.05.08 - 1.12.1
 - Fixed deprecation warnings from django 1.9 - thanks Maxim Tsoy

## 2014.09.11 - 1.12
 - Improved logging - thanks Alexander Kavanaugh (credits to https://github.com/yceruto/ for ExceptionReporter)

## 2014.09.01 - 1.11
 - fixed multi-column sorting - thanks Alexander Kavanaugh

## 2014.08.17 - 1.10
 - fixed handling of orderable/searchable for columns - were 'true'/'false' strings instead of bool
 - added error handling
 Thanks Roeland van Nieuwkerk for these

## 2014.06.22 - 1.9
 - converted the package to the use of the new camel case notation for DataTable 1.10 (http://www.datatables.net/upgrade/1.10-convert)
   (Derrick Jackson)

## 2014.04.03 - 1.8

 - use force_text for django 1.5 and python3
 - separate DatatableMixin mixin from BaseDatatableView

## 2013.11.20 - 1.7

 - enables the column list to contain values such as "foreignkey.value".

## 2013.07.18 - 1.6

- compatibility with django 1.5 (thanks restless_being for patch and ema93sh for review)

## 2013.06.15 - 1.5

- added some 'batteries included' to django_datatables_view, use DjangoJSONEncoder (thanks Ewoud Kohl van Wijngaarden)

## 2013.03.17 - 1.4

- add max_display_length parameter to allow easy customisation of max records limit (thanks Eric Gallimore)


## 2013.02.14 - 1.3

- added support for datatables with disabled pagination


## 2012.10.17 - 1.2

- added JSON encoder to handle lazy translations and Decimals


## 2012.10.17 - 1.1

- use request.REQUEST instead of request.POST
- remove unnecessary code
