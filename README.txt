
MobileMiddleware takes request and process a flag is_mobile with True or False.


Copyright (C) 2012 Hari Kishan<hari.kishan81001@gmail.com>
======================================

Overview :
========

MobileMiddleware is strong enough to identify  where request is coming  from? If you are requesting a URL from a mobile then it will identify the request and will raise the flag is_mobile=True then you can server a different template for the view of User.

Enable MobileMiddleware in your project :
=========================

	* Add Check_MobileRequest in your INSTALLED_APPS settings in settings.py file.
	* Add  Check_MobileRequest.middleware.Check_Mobile_request in your MIDDLEWARE_CLASSES 	   after the authentication and session middleware. 

How to use :
=========
	First import the middleware in your file as ::
		from    Check_MobileRequest.middleware import  Check_Mobile_request
	to use this class
                         if Check_Mobile_request().mobileBrowser( self.request ):
			###serve the template designed for mobile
		else:
			### serve the template designed for full view.


------------Done

Thanks

