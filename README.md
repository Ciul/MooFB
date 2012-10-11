MooBitly
========

Takes advantage of Bitly Link API to ease make use of it.

How to use
----------
	
	First you need to follow Bitly instructions on how to register an application.
	You can read about at http://dev.bitly.com/my_apps.html
	
	As a simple example, you could use the following lines at Document Head:
	It requires More/Request.JSONP class to work.
	
	<html>
		<head>
			<title>My Fantastic Facebook App</title>
			<script type="text/javascript" src="mootools-core.js" />
			<script type="text/javascript" src="mootools-more.js" /> <!-- Request.JSONP class required -->
			<script type="text/javascript" src="MooBitly.js" />
			
			[... whatever else you have in your document head]
		</head>
		
		<body>
			<!-- Your html code -->
		</body>
	</html>
	
	then use the Bitly app login and apiKey to create an instance of MooBitly this way:
	var moobitly = new MooBitly('myLogin', 'myApiKey');
	
	The complete documentation of Bitly API can be found at:
	http://dev.bitly.com/links.html
	
How to make api calls
---------------------
	
	After you MooBitly instace is created, you can call for api methods, like expand, info, lookup and shorten.
	All these methods expect a function to be called at onComplete event of the request made.
	
	moobitly.shorten('http://www.mywebsiteurl.com', null, function(response) {
		// Do something with api response here...
	});
	
	
	The MooBitly.js file is well documented with info of each method argument.
	
	MooBitly also has a caching feature if you use the id argument of methods, you can retrieve/remove the response of that call later.

	
QRcode
------	
	
	There is a (maybe not well known) Bitly feature for shortened url's, and this that Bitly can return QRcode image of shortened url's.
	
	To generate a QR code, simply append .qrcode to the end of any bitly link. For example: http://bit.ly/3eI7.qrcode
	QR codes of different sizes can be generated by adding ?s={size} to the QR code URL.
	A QR code of the closest standard size (in pixels) will be returned.
	
	Examples:
	<img src="http://bit.ly/cmeH01.qrcode" />
	<img src="http://bit.ly/cmeH01.qrcode?s=1000" /> <!-- For a 1000px (square) size image -->
	
	You can read more at:
	http://dev.bitly.com/qr_codes.html
	
Donations
---------
	
	Donations are welcome. By donating you contribute to this and other Open Source efforts.