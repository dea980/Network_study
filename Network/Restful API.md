Rest have 4 different functions : GET, POST, UPDATE, DELETE

Most of the programmers were using the REST architect because it has lost of benefit to use.
- For REST architecture there were 6 different constraints
	1. Uniform interface :  must be configured with a consistent interface. 
		- which means any other platform (Android, linux, IOS, etc) should be accessible through URI(Uniform Resource Identifier)
	2. Stateless
		- The server does not need to know the status of the client. (Which you do not maintain a session)
		- This is because Rest is HTTP communication, and you only need to submit the data when the client requests it.
		- So the client has been connected a few times, and the client doesn't need to know the server that has recently requested data.
	3. Cachable
		- Rest uses a basic HTTP method. this means that you can kesh in basic web communication.
		- When I access the Internet, images and documents are stored in the client cache, and the same request occurs.
		- Remove from the cache and use it rather than get it back from the server. It reduces the load on the server and increases the speed.
		- It can have an effect, and this feature is possible with HTTP communication.
		- Rest performs HTTP communication, so you can also use cache.
	4. Client -server Structure.
		- The roles of the client and server must be clearly divided. 
		- The server provides only the API, and the client provides login information, fine lines, and so on.
	5. Layered System
		- The client usually does not know whether it is connected directly to the target server or through an intermediated server.
		- The client just need to receive dat from the server. So each route to the server can include load balance or shared cache.
		- Useful for scaling up your system
	6.  Code Demand Constraint
		- REST can extend client functionally by downloading and executing code in the form of apps or scripts
		- Simplifying the client by reducing the number of features required for pre-implementation.
		- Downloading features after deployment improves system scalability.
		- Visibility is also reduced, which is an optional limitation within REST.
- Rest  have own rule
 1. every information demonstrated in URI 
	 1.  Get or Post or DELETE , path for the URI need to be same if it is same data.
2. For demonstrated the layer relation, need to use '/'
	1. ex) Get school/class, Post school/class, Delete school/class
3. Not use underbar( _ ) and use hyphen ( - )
	1. If you are using the underbar, characters may be obscured in the address window or readability may be impaired when the user reads it.
4. No spacing
	1. Spaces can also be less readable, causing users to become confused.
5. URI's expression in lowercase.
6. Do not display extensions in URI.
7. The expression of URI is a noun, in other words, it does not use verbs.
	1. ex) GET school/class // OK, GET school/ study // FAIL
8. Do not put '/' at the end of the UROI.
	1. ex) GET school/class // OK, GET school/class / / Fail.
