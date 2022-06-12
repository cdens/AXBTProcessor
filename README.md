# **AXBT Processor**

## Overview
The AXBT Processor can reprocess AXBT audio (WAV) files via command line, outputting a file containing AXBT signal data (signal level, peak frequency) and observed temperature versus depth. 


### Usage:
`python3 processAXBT -i inputfile.WAV`

### Installation and Setup:
This script requires python modules other than python base. Install them with `pip install -r requirements.txt`

### Optional flags:

<table>
  <tbody>
    <tr>
      <th align="center">Flag</th>
      <th align="left">Purpose</th>
    </tr>
    <tr>
      <td align="center">-o</td>
      <td>Output filename- full or relative path and filename for output AXBT drop metadata and profile file (defaults to <code>output.txt</code>)</td>
    </tr>
    <tr>
      <td align="center">-s</td>
      <td>Start time of AXBT profile in WAV file, format: SS, MM:SS, or HH:MM:SS (default: 0 sec)</td>
    </tr>
    <tr>
      <td align="center">-e</td>
      <td>End time of AXBT profile in WAV file, format: SS, MM:SS, or HH:MM:SS (default: end of WAV file)</td>
    </tr>  
    <tr>
      <td align="center">-a</td>
      <td>Input channel for audio file (1 for left, 2 for right, -1 to sum across all channels)</td>
    </tr>  
    <tr>
      <td align="center">-w</td>
      <td>Window length for each FFT (sec)</td>
    </tr>  
    <tr>
      <td align="center">-m</td>
      <td>Minimum signal level for good data (dB)</td>
    </tr>  
    <tr>
      <td align="center">-r</td>
      <td>Minimum signal ratio for good data (0-1)</td>
    </tr>  
    <tr>
      <td align="center">-a</td>
      <td>Minimum signal level to trigger profile collection (dB)</td>
    </tr>  
    <tr>
      <td align="center">-b</td>
      <td>Minimum signal ratio to trigger profile collection</td>
    </tr>  
    <tr>
      <td align="center">-t</td>
      <td>Frequency (Hz) to temperature (degC) conversion coefficients: [C<sub>0</sub>,C<sub>1</sub>,C<sub>2</sub>,C<sub>3</sub>] where T = C<sub>0</sub> + C<sub>1</sub>*f + C<sub>2</sub>*f<sup>2</sup> + C<sub>3</sub>*f<sup>3</sup></td>
    </tr>  
    <tr>
      <td align="center">-z</td>
      <td>Time elapsed (s) to depth (m) conversion coefficients: [C<sub>0</sub>,C<sub>1</sub>,C<sub>2</sub>,C<sub>3</sub>] where z = C<sub>0</sub> + C<sub>1</sub>*t + C<sub>2</sub>*t<sup>2</sup> + C<sub>3</sub>*t<sup>3</sup></td>
    </tr>  
    <tr>
      <td align="center">-f</td>
      <td>Minimum and maximum frequencies for good AXBT data: [min_f,max_f]</td>
    </tr>  
    </tbody>
</table>

<br />
<br />



## More Information

AXBT Processor uses the same algorithms implemented in the Airborne eXpendable Buoy Processing System (AXBPS) to process AXBT profiles from raw audio files. For more information, see the [AXBPS homepage](http://mmmfire.whoi.edu/axbps).


<br />

