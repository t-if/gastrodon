# Day Planner Status Colors

Change the colors of the chart in the [Day Planner](https://github.com/ivan-lednev/obsidian-day-planner) status bar widget.

### Snippet

Available for download [here](https://github.com/t-if/gastrodon/blob/main/Snippets/Originals/Coloring%20Book/Day%20Planner%20Status%20Colors.css).

```css
/* @settings

name: Day Planner Status Styling
id: day-planner-status-style
description: Change style of Day Planner's status bar widget.
settings:
    - 
        id: incomplete
        title: Incomplete Segment Color
        type: variable-themed-color
        format: hex
        default-light: '#'
        default-dark: '#'
    -
        id: complete
        title: Complete Segment Color
        type: variable-themed-color
        format: hex
        default-light: '#'
        default-dark: '#'
*/

/* bar */
.day-planner-progress-value {
    background-color: var(--complete);
}

.day-planner-progress-bar {
    background-color: var(--incomplete);
}


/* pie */
.progress-pie {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: var(--incomplete);
  background-image: linear-gradient(to right, transparent 50%, var(--complete) 0);
  position: relative;
  display: inline-block;
}
.progress-pie::after {
  background-color: var(--incomplete);
}
.progress-pie[data-value="0"]:before {
  transform: rotate(0turn);
}
.progress-pie[data-value="1"]:before {
  transform: rotate(0.01turn);
}
.progress-pie[data-value="2"]:before {
  transform: rotate(0.02turn);
}
.progress-pie[data-value="3"]:before {
  transform: rotate(0.03turn);
}
.progress-pie[data-value="4"]:before {
  transform: rotate(0.04turn);
}
.progress-pie[data-value="5"]:before {
  transform: rotate(0.05turn);
}
.progress-pie[data-value="6"]:before {
  transform: rotate(0.06turn);
}
.progress-pie[data-value="7"]:before {
  transform: rotate(0.07turn);
}
.progress-pie[data-value="8"]:before {
  transform: rotate(0.08turn);
}
.progress-pie[data-value="9"]:before {
  transform: rotate(0.09turn);
}
.progress-pie[data-value="10"]:before {
  transform: rotate(0.1turn);
}
.progress-pie[data-value="11"]:before {
  transform: rotate(0.11turn);
}
.progress-pie[data-value="12"]:before {
  transform: rotate(0.12turn);
}
.progress-pie[data-value="13"]:before {
  transform: rotate(0.13turn);
}
.progress-pie[data-value="14"]:before {
  transform: rotate(0.14turn);
}
.progress-pie[data-value="15"]:before {
  transform: rotate(0.15turn);
}
.progress-pie[data-value="16"]:before {
  transform: rotate(0.16turn);
}
.progress-pie[data-value="17"]:before {
  transform: rotate(0.17turn);
}
.progress-pie[data-value="18"]:before {
  transform: rotate(0.18turn);
}
.progress-pie[data-value="19"]:before {
  transform: rotate(0.19turn);
}
.progress-pie[data-value="20"]:before {
  transform: rotate(0.2turn);
}
.progress-pie[data-value="21"]:before {
  transform: rotate(0.21turn);
}
.progress-pie[data-value="22"]:before {
  transform: rotate(0.22turn);
}
.progress-pie[data-value="23"]:before {
  transform: rotate(0.23turn);
}
.progress-pie[data-value="24"]:before {
  transform: rotate(0.24turn);
}
.progress-pie[data-value="25"]:before {
  transform: rotate(0.25turn);
}
.progress-pie[data-value="26"]:before {
  transform: rotate(0.26turn);
}
.progress-pie[data-value="27"]:before {
  transform: rotate(0.27turn);
}
.progress-pie[data-value="28"]:before {
  transform: rotate(0.28turn);
}
.progress-pie[data-value="29"]:before {
  transform: rotate(0.29turn);
}
.progress-pie[data-value="30"]:before {
  transform: rotate(0.3turn);
}
.progress-pie[data-value="31"]:before {
  transform: rotate(0.31turn);
}
.progress-pie[data-value="32"]:before {
  transform: rotate(0.32turn);
}
.progress-pie[data-value="33"]:before {
  transform: rotate(0.33turn);
}
.progress-pie[data-value="34"]:before {
  transform: rotate(0.34turn);
}
.progress-pie[data-value="35"]:before {
  transform: rotate(0.35turn);
}
.progress-pie[data-value="36"]:before {
  transform: rotate(0.36turn);
}
.progress-pie[data-value="37"]:before {
  transform: rotate(0.37turn);
}
.progress-pie[data-value="38"]:before {
  transform: rotate(0.38turn);
}
.progress-pie[data-value="39"]:before {
  transform: rotate(0.39turn);
}
.progress-pie[data-value="40"]:before {
  transform: rotate(0.4turn);
}
.progress-pie[data-value="41"]:before {
  transform: rotate(0.41turn);
}
.progress-pie[data-value="42"]:before {
  transform: rotate(0.42turn);
}
.progress-pie[data-value="43"]:before {
  transform: rotate(0.43turn);
}
.progress-pie[data-value="44"]:before {
  transform: rotate(0.44turn);
}
.progress-pie[data-value="45"]:before {
  transform: rotate(0.45turn);
}
.progress-pie[data-value="46"]:before {
  transform: rotate(0.46turn);
}
.progress-pie[data-value="47"]:before {
  transform: rotate(0.47turn);
}
.progress-pie[data-value="48"]:before {
  transform: rotate(0.48turn);
}
.progress-pie[data-value="49"]:before {
  transform: rotate(0.49turn);
}
.progress-pie[data-value="50"]:before {
  transform: rotate(0.5turn);
}
.progress-pie[data-value="51"]:before {
  background-color: var(--complete);
  transform: rotate(0.01turn);
}
.progress-pie[data-value="52"]:before {
  background-color: var(--complete);
  transform: rotate(0.02turn);
}
.progress-pie[data-value="53"]:before {
  background-color: var(--complete);
  transform: rotate(0.03turn);
}
.progress-pie[data-value="54"]:before {
  background-color: var(--complete);
  transform: rotate(0.04turn);
}
.progress-pie[data-value="55"]:before {
  background-color: var(--complete);
  transform: rotate(0.05turn);
}
.progress-pie[data-value="56"]:before {
  background-color: var(--complete);
  transform: rotate(0.06turn);
}
.progress-pie[data-value="57"]:before {
  background-color: var(--complete);
  transform: rotate(0.07turn);
}
.progress-pie[data-value="58"]:before {
  background-color: var(--complete);
  transform: rotate(0.08turn);
}
.progress-pie[data-value="59"]:before {
  background-color: var(--complete);
  transform: rotate(0.09turn);
}
.progress-pie[data-value="60"]:before {
  background-color: var(--complete);
  transform: rotate(0.1turn);
}
.progress-pie[data-value="61"]:before {
  background-color: var(--complete);
  transform: rotate(0.11turn);
}
.progress-pie[data-value="62"]:before {
  background-color: var(--complete);
  transform: rotate(0.12turn);
}
.progress-pie[data-value="63"]:before {
  background-color: var(--complete);
  transform: rotate(0.13turn);
}
.progress-pie[data-value="64"]:before {
  background-color: var(--complete);
  transform: rotate(0.14turn);
}
.progress-pie[data-value="65"]:before {
  background-color: var(--complete);
  transform: rotate(0.15turn);
}
.progress-pie[data-value="66"]:before {
  background-color: var(--complete);
  transform: rotate(0.16turn);
}
.progress-pie[data-value="67"]:before {
  background-color: var(--complete);
  transform: rotate(0.17turn);
}
.progress-pie[data-value="68"]:before {
  background-color: var(--complete);
  transform: rotate(0.18turn);
}
.progress-pie[data-value="69"]:before {
  background-color: var(--complete);
  transform: rotate(0.19turn);
}
.progress-pie[data-value="70"]:before {
  background-color: var(--complete);
  transform: rotate(0.2turn);
}
.progress-pie[data-value="71"]:before {
  background-color: var(--complete);
  transform: rotate(0.21turn);
}
.progress-pie[data-value="72"]:before {
  background-color: var(--complete);
  transform: rotate(0.22turn);
}
.progress-pie[data-value="73"]:before {
  background-color: var(--complete);
  transform: rotate(0.23turn);
}
.progress-pie[data-value="74"]:before {
  background-color: var(--complete);
  transform: rotate(0.24turn);
}
.progress-pie[data-value="75"]:before {
  background-color: var(--complete);
  transform: rotate(0.25turn);
}
.progress-pie[data-value="76"]:before {
  background-color: var(--complete);
  transform: rotate(0.26turn);
}
.progress-pie[data-value="77"]:before {
  background-color: var(--complete);
  transform: rotate(0.27turn);
}
.progress-pie[data-value="78"]:before {
  background-color: var(--complete);
  transform: rotate(0.28turn);
}
.progress-pie[data-value="79"]:before {
  background-color: var(--complete);
  transform: rotate(0.29turn);
}
.progress-pie[data-value="80"]:before {
  background-color: var(--complete);
  transform: rotate(0.3turn);
}
.progress-pie[data-value="81"]:before {
  background-color: var(--complete);
  transform: rotate(0.31turn);
}
.progress-pie[data-value="82"]:before {
  background-color: var(--complete);
  transform: rotate(0.32turn);
}
.progress-pie[data-value="83"]:before {
  background-color: var(--complete);
  transform: rotate(0.33turn);
}
.progress-pie[data-value="84"]:before {
  background-color: var(--complete);
  transform: rotate(0.34turn);
}
.progress-pie[data-value="85"]:before {
  background-color: var(--complete);
  transform: rotate(0.35turn);
}
.progress-pie[data-value="86"]:before {
  background-color: var(--complete);
  transform: rotate(0.36turn);
}
.progress-pie[data-value="87"]:before {
  background-color: var(--complete);
  transform: rotate(0.37turn);
}
.progress-pie[data-value="88"]:before {
  background-color: var(--complete);
  transform: rotate(0.38turn);
}
.progress-pie[data-value="89"]:before {
  background-color: var(--complete);
  transform: rotate(0.39turn);
}
.progress-pie[data-value="90"]:before {
  background-color: var(--complete);
  transform: rotate(0.4turn);
}
.progress-pie[data-value="91"]:before {
  background-color: var(--complete);
  transform: rotate(0.41turn);
}
.progress-pie[data-value="92"]:before {
  background-color: var(--complete);
  transform: rotate(0.42turn);
}
.progress-pie[data-value="93"]:before {
  background-color: var(--complete);
  transform: rotate(0.43turn);
}
.progress-pie[data-value="94"]:before {
  background-color: var(--complete);
  transform: rotate(0.44turn);
}
.progress-pie[data-value="95"]:before {
  background-color: var(--complete);
  transform: rotate(0.45turn);
}
.progress-pie[data-value="96"]:before {
  background-color: var(--complete);
  transform: rotate(0.46turn);
}
.progress-pie[data-value="97"]:before {
  background-color: var(--complete);
  transform: rotate(0.47turn);
}
.progress-pie[data-value="98"]:before {
  background-color: var(--complete);
  transform: rotate(0.48turn);
}
.progress-pie[data-value="99"]:before {
  background-color: var(--complete);
  transform: rotate(0.49turn);
}
.progress-pie[data-value="100"]:before {
  background-color: var(--complete);
  transform: rotate(0.5turn);
}
```
