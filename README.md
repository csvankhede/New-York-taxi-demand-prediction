# New York taxi demand prediction

![new york taxi demand prediction](https://user-images.githubusercontent.com/25454660/62773719-82a74c00-bac0-11e9-9f6b-c0fb4dd64bb3.jpg)

This is a case study of New York taxi demand prediction where time series data is used.

### Problem statement
To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.
To solve the above problem data collected in Jan - Mar 2015 is used to predict the pickups in Jan - Mar 2016.

### Type of problem
Time-series forecasting and Regression

### Data Information
Ge the data from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml (2016 data) The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)
### Features in the dataset:
<table border="1">
    <tbody><tr>
        <th>Field Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>VendorID</td>
        <td>
        A code indicating the TPEP provider that provided the record.
        <ol>
            <li>Creative Mobile Technologies</li>
            <li>VeriFone Inc.</li>
        </ol>
        </td>
    </tr>
    <tr>
        <td>tpep_pickup_datetime</td>
        <td>The date and time when the meter was engaged.</td>
    </tr>
    <tr>
        <td>tpep_dropoff_datetime</td>
        <td>The date and time when the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Passenger_count</td>
        <td>The number of passengers in the vehicle. This is a driver-entered value.</td>
    </tr>
    <tr>
        <td>Trip_distance</td>
        <td>The elapsed trip distance in miles reported by the taximeter.</td>
    </tr>
    <tr>
        <td>Pickup_longitude</td>
        <td>Longitude where the meter was engaged.</td>
    </tr>
    <tr>
        <td>Pickup_latitude</td>
        <td>Latitude where the meter was engaged.</td>
    </tr>
    <tr>
        <td>RateCodeID</td>
        <td>The final rate code in effect at the end of the trip.
        <ol>
            <li> Standard rate </li>
            <li> JFK </li>
            <li> Newark </li>
            <li> Nassau or Westchester</li>
            <li> Negotiated fare </li>
            <li> Group ride</li>
        </ol>
        </td>
    </tr>
    <tr>
        <td>Store_and_fwd_flag</td>
        <td>This flag indicates whether the trip record was held in vehicle memory before sending to the vendor, aka “store and forward,” because the vehicle did not have a connection to the server.
  <br>Y= store and forward trip
    <br> N= not a store and forward trip
   </td>
  </tr>
    <tr>
        <td>Dropoff_longitude</td>
        <td>Longitude where the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Dropoff_ latitude</td>
        <td>Latitude where the meter was disengaged.</td>
    </tr>
    <tr>
        <td>Payment_type</td>
        <td>A numeric code signifying how the passenger paid for the trip.
        <ol>
            <li> Credit card </li>
            <li> Cash </li>
            <li> No charge </li>
            <li> Dispute</li>
            <li> Unknown </li>
            <li> Voided trip</li>
        </ol>
        </td>
    </tr>
    <tr>
        <td>Fare_amount</td>
        <td>The time-and-distance fare calculated by the meter.</td>
    </tr>
    <tr>
        <td>Extra</td>
        <td>Miscellaneous extras and surcharges. Currently, this only includes. the <span class="MathJax_Preview" style="color: inherit; display: none;"></span><span class="MathJax" id="MathJax-Element-1-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>0.50</mn><mi>a</mi><mi>n</mi><mi>d</mi></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true"><span class="math" id="MathJax-Span-1" style="width: 4.17em; display: inline-block;"><span style="display: inline-block; position: relative; width: 3.455em; height: 0px; font-size: 120%;"><span style="position: absolute; clip: rect(1.313em, 1003.46em, 2.384em, -999.997em); top: -2.199em; left: 0em;"><span class="mrow" id="MathJax-Span-2"><span class="mn" id="MathJax-Span-3" style="font-family: MathJax_Main;">0.50</span><span class="mi" id="MathJax-Span-4" style="font-family: MathJax_Math-italic;">a</span><span class="mi" id="MathJax-Span-5" style="font-family: MathJax_Math-italic;">n</span><span class="mi" id="MathJax-Span-6" style="font-family: MathJax_Math-italic;">d<span style="display: inline-block; overflow: hidden; height: 1px; width: 0.003em;"></span></span></span><span style="display: inline-block; width: 0px; height: 2.205em;"></span></span></span><span style="display: inline-block; overflow: hidden; vertical-align: -0.068em; border-left: 0px solid; width: 0px; height: 1.004em;"></span></span></nobr><span class="MJX_Assistive_MathML" role="presentation"><math xmlns="http://www.w3.org/1998/Math/MathML"><mn>0.50</mn><mi>a</mi><mi>n</mi><mi>d</mi></math></span></span><script type="math/tex" id="MathJax-Element-1">0.50 and </script>1 rush hour and overnight charges.</td>
    </tr>
    <tr>
        <td>MTA_tax</td>
        <td>0.50 MTA tax that is automatically triggered based on the metered rate in use.</td>
    </tr>
    <tr>
        <td>Improvement_surcharge</td>
        <td>0.30 improvement surcharge assessed trips at the flag drop. the improvement surcharge began being levied in 2015.</td>
    </tr>
    <tr>
        <td>Tip_amount</td>
        <td>Tip amount – This field is automatically populated for credit card tips.Cash tips are not included.</td>
    </tr>
    <tr>
        <td>Tolls_amount</td>
        <td>Total amount of all tolls paid in trip.</td>
    </tr>
    <tr>
        <td>Total_amount</td>
        <td>The total amount charged to passengers. Does not include cash tips.</td>
    </tr>
</tbody></table>

