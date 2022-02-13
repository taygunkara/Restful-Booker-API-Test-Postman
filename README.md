# Restful  Booker API Testing with Postman & Newman

[Restful-booker](http://restful-booker.herokuapp.com/API ) is a Create Read Update Delete Web API that comes with authentication features and loaded with a bunch of bugs for you to explore.
testing and tools website.

---
## Tasks
- Auth
	- CreateToken
- Booking
	- GetBookingIds
	- GetBooking
	- CreateBooking
	- UpdateBooking
	- PartialUpdateBooking
	- DeleteBooking
- Ping
	- HealthCheck


## Dependencies
- `npm`, `nodejs`, `newman`, `jenkins(optional)`
---

## Usage

1. Download json file and run this command.
	
```
newman run Restful-Booker.postman_collection.json \
--environment "https://api.getpostman.com/environments/17544637-2a99e17a-8b5b-4c44-aeb2-43279b297e7d?apikey=PMAK-6208e3dddb474123cb1acc46-f22ef29718c15d8c61a03d31829a9f97dc" 
```

2. Run this command in your shell.

```
newman run "https://api.getpostman.com/collections/17544637-aa5c75e6-992e-4738-b076-dc8bb1e3fbbc?apikey=PMAK-6208e3dddb474123cb1acc46-f22ef29718c15d8c61a03d31829a9f97dc" \
--environment "https://api.getpostman.com/environments/17544637-2a99e17a-8b5b-4c44-aeb2-43279b297e7d?apikey=PMAK-6208e3dddb474123cb1acc46-f22ef29718c15d8c61a03d31829a9f97dc" 
```

3. Intagrate with Jenkins and Automate test and create junit report.
	
```
newman run "https://api.getpostman.com/collections/17544637-aa5c75e6-992e-4738-b076-dc8bb1e3fbbc?apikey=PMAK-6208e3dddb474123cb1acc46-f22ef29718c15d8c61a03d31829a9f97dc" \
--environment "https://api.getpostman.com/environments/17544637-2a99e17a-8b5b-4c44-aeb2-43279b297e7d?apikey=PMAK-6208e3dddb474123cb1acc46-f22ef29718c15d8c61a03d31829a9f97dc" \
-r cli,junit \
--reporter-junit-export "newman/restful-booker.xml"
```
 
[API Documentation](http://restful-booker.herokuapp.com/apidoc/index.html)