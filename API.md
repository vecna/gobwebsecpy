# API to use

  * paraguay
    * https://invi.sible.link/api/v1/surface/gov.paraguay
    * https://invi.sible.link/api/v1/details/gov.paraguay
    * https://invi.sible.link/api/v1/extended/gov.paraguay
  * brasil
    * https://invi.sible.link/api/v1/surface/gov.brasil
    * https://invi.sible.link/api/v1/details/gov.brasil
    * https://invi.sible.link/api/v1/extended/gov.brasil
  * chile
    * https://invi.sible.link/api/v1/surface/gov.chile
    * https://invi.sible.link/api/v1/details/gov.chile
    * https://invi.sible.link/api/v1/extended/gov.chile
  * colombia
    * https://invi.sible.link/api/v1/surface/gov.colombia
    * https://invi.sible.link/api/v1/details/gov.colombia
    * https://invi.sible.link/api/v1/extended/gov.colombia


Every list of website has a name, I call if "campaign name", in this example, is gov.paraguay, but normally is better if is the name of the country analyzed. 

JSON Pretty Print: http://jsonprettyprint.com/

## API "surface" https://invi.sible.link/api/v1/surface/gov.paraguay

It return: ONE object per every SITE TESTED (if converted in CSV, is one line per site tested)
        

    url: "http://www.presidencia.gov.py/
    	name of the website tested
    unrecognized: []
    	third party DOMAIN NAMED whitout a clear attribution to a known company (for example, you will never see here google-analytic, because it is attributed to Google)
    when: "2018-03-01T00:00:00.000Z"
    	day in which the test has been done
    cookies: [ "presidencia.gov.py", "youtube.com"]
    	is a LIST, and contain all the domain named which have installed a cookie in the browser
    leaders: [ { company: "Google", country: "US", p: 83.33 }]
    	is a LIST of OBJECT, every object contains:
			company: the name of the company found
			country: if has a country attribution, e.g. where the headquarter are (otherwise is UNKNOWN)
			p: the percentage: among all the website tested in gov.paraguay, 83% have google.


## API "details" https://invi.sible.link/api/v1/details/gov.paraguay

ONE object per every THIS PARTY INCLUSION, this mean, you should find for every website many entry as much as are the third parties included.
This API contains technical details on the javascript behavior. namely, the script who can profile the browser without using cookies, like the one used in https://panopticlick.eff.org/

    href: "http://www.presidencia.gov.py" 
    	name of the website tested
    inclusion: "www.youtube.com" 
    	This is the website included which executes these javascript commands:
    Date_prototype_getTimezoneOffset 1 
    navigator_plugins 6 
    navigator_userAgent 4 
    screen_availWidth 1 
    screen_colorDepth 1 
    screen_width 1 
    window_devicePixelRatio 10 
    window_localStorage 3 
    window_sessionStorage 1 
    	Instead of the "_" you should replace with "." and that is the javascript command executed by youtube, window.sessionStorage is a command to access on storage area of the browser, and store tracking code or just do other operations.


    subjectId "cf9477667388160db3c7e1a0681fe16fdd7589de" 
		this identify the tested website, do not change with time, will be the same also in the next days
    when "2018-03-01T00:00:00.000Z" 
    campaign "gov.paraguay"


## API "extended" https://invi.sible.link/api/v1/extended/gov.paraguay

ONE object per every THIS PARTY INCLUSION, this mean, you should find for every website many entry as much as are the third parties included.


    url: "https://static.xx.fbcdn.àv3/yO/r/kjb-FcLGuO4.png"
    URL of the third party resource included
    requestTime: "2018-02-28T01:02:39.144Z"
    	moment in which the test has been performed
    Content-Type: "image/png"
    	type of the third party resource included
    Expires: "2019-02-26T21:56:31.000Z"
    	if has caching: how much it last alive. 
    Content-Length: 2604
    	size of the resource
    subjectId: "a10223ccf705c05b2f7ebb30911634eb796b9fcb"
    	this identify the tested website, do not change with time, will be the same also in the next days
    href: "https://www.senatics.gov.py"
    	tested site
    domaindottld: "fbcdn.net"
    	domain named of the third party resource
    company: "Facebook"
    companyC: "US"
    when: "2018-02-28T00:00:00.000Z"
    product: "Facebook"

