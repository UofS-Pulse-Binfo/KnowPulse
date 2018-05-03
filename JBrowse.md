## Customization
We have changed the colours of our JBrowse to make it match KnowPulse for more seamless integration. 
The following diff's show the changes that have been made (line numbers refer to v1.12.0):

### main.css
```diff
226c226
<     border-bottom-color: #17313E;
---
>     border-bottom-color: #A9C6EB;
234c234
<     border: 2px solid #17313E;
---
>     border: 2px solid red;
```

### menubar.css
```diff
7,8c7
<     background-color: #132A37;
<     background: url('http://knowpulse.usask.ca/portal/sites/all/themes/kptheme/images/mainbarbg.jpg') repeat-x;
---
>     background: #396494;
```

### track_styles.css
```diff
120c120
<     height: 1px;
---
>     height: 7px;
125c125
<     background-color: #4C4C4C;
---
>     background-color: #62d335;
446,447c446,450
<     height: 10px;
<     background-color: #00FF00;
---
>     height: 4px;
>     background-color: #66B;
>     border-style: solid;
>     border-color: #88D;
>     border-width: 2px 0px 2px 0px;
```
