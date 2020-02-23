
Only the client can choose a random port for itself before it connects to the server.
It is normal and typical behavior for a client to use a random outbound port. To change that, you have to bind socket to a specifuc port before calling connect with the server.


the OS chooses an appropriate network adapter and assigns its IP if not explicitly stated,
and assigns a random available ephemeral port if not explicitly stated.