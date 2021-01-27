editable-table
=================

This tiny (5.6KB, 200 lines, 3.2KB minified) jQuery plugin turns any table into an editable spreadsheet. Here are the key features:

* No magic - works on a normal HTML table (so you can plug it in into any web
table)
* Supports validation and change events (so you can warn about invalid input or
prevent invalid changes)
* Uses standard DOM focus for selection (so does not interrupt scrolling or
tabbing outside the table)
* Native copy/paste support
* Does not force any styling (so you can style it any way you want, using normal
CSS)
* Works well with Bootstrap

Basic Usage
-----------

### HTML

    <table id="secondDemo" class="table table-striped">
      <thead><tr>
        <th>Location</th>
        <th>Expires</th>
        <th>Count</th>
        <th>Value</th>
      </tr></thead>
      <tbody>
        <tr>
          <td data-edit-type="select" data-edit-source="locations">Adelaide</td>
          <td data-edit-type="date">24-Jan-2015</td>
          <td data-edit-type="ntext">8</td>
          <td data-edit-type="vtext">5,000</td>
        </tr>
        <tr>
          <td data-edit-type="select" data-edit-source="locations">Brisbane</td>
          <td data-edit-type="date">25-Jan-2015</td>
          <td data-edit-type="ntext">8</td>
          <td data-edit-type="vtext">15,000</td>
        </tr>
        <tr>
          <td data-edit-type="select" data-edit-source="locations">Melbourne</td>
          <td data-edit-type="date">26-Jan-2015</td>
          <td data-edit-type="ntext">9</td>
          <td data-edit-type="vtext">8,000</td>
        </tr>
        <tr>
          <td data-edit-type="select" data-edit-source="locations">Sydney</td>
          <td data-edit-type="date">27-Jan-2015</td>
          <td data-edit-type="ntext">6</td>
          <td data-edit-type="vtext">9,000</td>
        </tr>
      </tbody>
    </table>

### Javascript

    var locations = {
        'Adelaide': 'Adelaide - South Australia',
        'Brisbane': 'Brisbane - Queensland',
        'Canberra': 'Canberra - Australian Capital Territory',
        'Darwin': 'Darwin - Northern Territory',
        'Hobart': 'Hobart - Tasmania',
        'Melbourne': 'Melbourne - Victoria',
        'Perth': 'Perth - Western Australia',
        'Sydney': 'Sydney - New South Wales'
    };
    $('#secondDemo').editableTableWidget();

Dependencies
------------
* jQuery http://jquery.com/
* Numeral https://github.com/adamwdraper/Numeral-js
* bootstrap-datepicker https://github.com/eternicode/bootstrap-datepicker
