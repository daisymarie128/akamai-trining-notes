

## Secure delivery
SSL: secure socket layer - 1.0, 2.0, 3.0
TLS Transport Layer Security
HTTPS: Hypertext Transfer Protocol Secure

### Certificates
- Clienst need ro check servers certs
- Akamai does both
-
- TLS: Mandate for US government site sto be secure
- Google SEO rankings for HTTPS-enabled sites
- HTTPS2 requires HTTPS
- Non HTTTPS sites makred as insecure

		Validation types:
		* ordered in least validation and least expensive*
		- Domain validation (DV) 
			- Must prove domain control only
		- Oraganization validation (OV)
			- Prove domain control + pass organizational vetting
		- Extended validation (EV)
			- Domain control
			- Extended 
			- CA verifies physical existance and integrity
			- Sites contain most prevelant visual cues
				- Org identified in green 
				
#### Cert types:
- Singleton
	- Only single entry allowed
- SAN 
-		Multip domains
- Wildcard
-		supports unlimited subdomains
-		Only sinle entry allowed
- Wildcard SAN
-		Multi domain and/or wildcard entries

## Caching

	Caching happens at the edge:
	- create caching rules
	- requires creating match conditions
	- do pre fetching
	- create behaviors
		- This will have a bunch of diff optins
			- Bypass cache: Good for debug options - ignores caching rules and gets new updates
	
### Downstream caching
This is used for caching the browser

### Cache Key

	Conatins host key
	- Can contain Paramteres
	- Path of obj
	- Query string
	- Additional info*

### Debug headers
I have no idea what their talking about
Research this
 

### Caching challenges

	When defining rules:
	- becareful what your caching - sensitive data
	-
	Caching of the client:
	- Some browsers have caching limits
	- Lose control over caching
	- Accidentally setting age limits (ie a year) can't be changed

## Content refreshing
	
	Methos:
	- 2 types
		- Purge
			- Fully deltes objects from AKamai network
			- Results full obj payload being fetched from Origin
		- Invalidate
			- Marks objs as expired - requiring re-validation before serving
			- Revalidation is done via - if-modified-Since request
			- Objs that have not changed can be revalidated by a mere header-only response
			-
	
	Tools: 
	- Fast Purge
	- Content Contrul Utility
	- Enhance Content control utility

## User insights

	Metric data:
	DNS
	TCP
	First byte

	Synthetic testing
	- backbone test
	- Useful for testing non production or smaller sites
	
	Real user testing
	- uses real testeres 
	-
	Real user measurments
	- RUM + JS
	- Great for mesuring real user measurments
	- Better insights into a wide variety of use cases and environments. ie diff browsers or devices etc
		use: ?akamairum=on
