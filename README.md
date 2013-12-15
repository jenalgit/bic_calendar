BIC Calendar
============

en - BIC Calendar is a simple calendar to mark events and ranges of dates, a jQuery plugin and Twitter Bootstrap.
For more info check: [http://bichotll.github.io/bic_calendar/](http://bichotll.github.io/bic_calendar/)

ca - BIC Calendar es un simple calendari per marcar esdeveniments i rangs de dates. Un plugin de jQuery i Twitter Bootstrap.
Per mes info: [http://bichotll.github.io/bic_calendar/](http://bichotll.github.io/bic_calendar/)

Dependencies
------------

- ~jQuery 1.7.2
- ~Twitter Bootstrap 3.0


Options
-------

- events (array of event object)

- dayNames (array)
    - default: ["l", "m", "x", "j", "v", "s", "d"]

- monthNames (array)
    - default: ["Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio", "Julio", "Agosto", "Septiembre", "Octubre", "Noviembre", "Diciembre"]

- showDays (boolean)
    - default: true

- reqAjax (json array of event array)
    - reqAjax.type (string) {'get', 'post'}
    - reqAjax.url (string)

- enableSelect (boolean)
    - default: false

- multiSelect (boolean)
    - default: false

- displayMonthController (boolean)
    - default: true

- displayYearController (boolean)
    - default: true

- popoverOptions (popover Twitter Bootstrap object)

- tooltipOptions (tooltip Twitter Bootstrap object)


Event object
----------------------------

- date(string):
    - "17/8/1989"
- title (string)
    - "Event Barberà"
- link (string)
    - "http://google.es"
- color(string)
    - "#333"
- class (string)
    - "activo congreso"
- content (string)
    - "Text for the content of popover...description of event...image..."

* if content is not defined it will be a tooltip


Event bicCalendarSelect
-----------------------------------

### Response

 - detail.dateFirst
    - 12/26/1989
 - detail.dateLast
    - 12/12/1992

### Example code events

```
document.addEventListener('bicCalendarSelect', function(e) {
    moment.lang('es'); // default the language to English
    var dateFirst = new moment(e.detail.dateFirst);
    var dateLast = new moment(e.detail.dateLast);

    $('#from-day').val(dateFirst.format('LL'));
    $('#to-day').val(dateLast.format('LL'));

});
```
