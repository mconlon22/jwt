Now require auth by registering at the endpoint 

178.62.61.92:4001/register 

with an example body of 

            {
                "first_name":"martin",
                "last_name":"conlon",
                "email":"martinconlon2222@gmail.com",
                "password":"helloworld"
            }
this will return you with 

            {
                "_id": "6166f017ced979236faa4b72",
                "first_name": "martin",
                "last_name": "conlon",
                "email": "martinconlon2222@gmail.com",
                "password": "$2b$10$kwVJKZ8onlTFiAu25cwxqeLIRFNWEWIZxQjTvGA290EJDBmmXS.8e",
                "__v": 0,
                "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoiNjE2NmYwMTdjZWQ5NzkyMzZmYWE0YjcyIiwiZW1haWwiOiJtYXJ0aW5jb25sb24yMjIyQGdtYWlsLmNvbSIsImlhdCI6MTYzNDEzNzgwOSwiZXhwIjoxNjM0MTQ1MDA5fQ.4ArOfytVCZWa6Z-08pqPOfH6gmLdP9FlWtHPn0oHMAs"
            }
you will need to take the token from here in order to send it as the x-access-token in the header for all of the requests to 
the mock server


once you have registered you can get a new token by sending a request to 
178.62.61.92:4001/login

with an example raw body of 

{
    "email":"martinconlon2222@gmail.com",
    "password":"helloworld"
}

which will return the same as above with the token needed for the requests to the mock server
