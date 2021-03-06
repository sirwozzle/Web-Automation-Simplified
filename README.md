## Description:
A way to make web automation with selenium simpler, by dynamically finding x_path of element by name
currently a work in progress

## Setup:
Run setup.sh
Install chromedriver or geckodriver
To change between chrome or firefox change the "chrome=True to chrome=False" in the template code of gen_py_test.py


## Usage:

To test if element is present:
```
    {"element text":"present"},
    {"element id":["by_id","present"]},
    {"element text":["by_string","present"]},
    {"element xpath":["by_xpath","present"]},
    {"element css selector":["by_css_selector","present"]},
```

To click on an element:
```
    Clicking on an element will also check that it is present before clicking
    {"element text":"click"},
    {"element id":["by_id","click"]},
    {"element text":["by_string","click"]},
    {"element xpath":["by_xpath","click"]},
    {"element css selector":["by_css_selector","click"]},
```

To send keys:
```
    {"element id":["by_id","keys","text to send as keys"]},
    {"element text":["by_string","keys","text to send as keys"]},
    {"element xpath":["by_xpath","keys","text to send as keys"]},
    {"element css selector":["by_css_selector","keys","text to send as keys"]},

    put "CODE:UP","CODE:DOWN","CODE:ENTER" to send up, down or enter keys (for dropdown navigation)
```
To upload a file via a browse for file button:
```
    {"xpath of button":["by_xpath","upload","file name in the /files dir"]},
```

To test if element is not_present:
```
    {"element text":"not_present"},
    {"element id":["by_id","not_present"]},
    {"element text":["by_string","not_present"]},
    {"element xpath":["by_xpath","not_present"]},
    {"element css selector":["by_css_selector","not_present"]},
```

To test the url is correct:
```
    {"url including https://....":"url"},
```
To go to a url:
``
    {"url including https://....":"goto"},
``

Waiting:
```
    {"wait":"#"} where # is the number of seconds to wait
    {"element text":"wait_until_not_present"},
    {"element text":"wait_until_present"},
```
To go back a page:
```
    {"back":"back"},
```
To print a message:
```
    {"message to print":"debug"}
    or
    {"message to print":"print"}
```


### Making a json

```{
  "test":[

PUT LINES DESC ABOVE HERE

  ]
}
```
make a test json and put in test-data folder, then run the "Run_all_Tests.py" to run

running tests
either run the "Run_All_Tests.py" in the tests folder
or run the "gen_py_test.py" and
run the respective python file for the json you want to run






