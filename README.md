##What is this?
An extremely simple to use CodeIgniter library that handles location geocoding and reverse geocoding.

##What do I need to use it?
You'll need to sign up for a [<http://developer.mapquest.com/>]() app key.

**Please note that it takes about an hour before the key becomes valid.**

##How do I use it?

####Add your Mapquest app key to your config/config.php: 	
	$config['mapquest_app_key'] = '';
	
####Load the library

	$this->load->library('geocoder');
	
####Call the methods in the library
	$this->geocoder->geocode($address); // To convert an address to lat/lng
	$this->geocoder->reverse_geocode($lat, $lng); // To convert a lat/lng to an address
 
##How to convert lat/lng to an address

	$address_details = $this->geocoder->reverse_geocode($lat, $lng);
	print_r($address_details); // This will show you relevant address details.

##How to convert an address to lat/lng
	
	$address_details = $this->geocoder->geocode($address);
	print_r($address_details); // This will show you relevant address details.

##Questions? Comments?

	Email me: me[at]raphaelcaixeta.com.
	Twitter: @raphaelcaixeta
