	- SQLite
		- SQLite is a in-process library that contains self-contained, serverless, zero-configuration, transactional SQL Database.

		- SQLite is anembedded SQL databse engine.

		- SQLite Reads and write data directly to ordinary disc files.

		- The Databare file formate is cross-platform(copy between 32 to 64 bit system).

		- There is no SQL queries validation during the compile time.

		- Lot of boiler plate code to convert SQL quries to Java object

		- It does not support RXjava or any reactive frame works

	- Room
		- Room persistence library provides an abstraction layer over the SQLite to allow more robust database access.

		- This helps you to create an cache of your app data on the device thats running your app.

		- Room is an ORM (Object Relational mapping library). This will map our database object to java objects.

		- There is an SQL queries validation at compile time.

		- Lesser code to convert SQL queries to Java object.

		- Room is built to work with live data and RXjava for data observation.