Remotely Accessing Server from a Client System using SSH:
	ssh-keygen -t ed25519 -C "email@gmail.com"
	--This generates a key and safely store it on the client system
	ssh-copy-id serverUser@serverIP
	--This establishes the connection with the server by copying the public key to the server
	--ASKS FOR THE SERVER PASSWORD TO CONNECT!
	scp serverUser@serverIP:[Path of File to be copied] .
	--This downloads the file from the server, the '.' at the end is to download the file in the current working directory
	scp -r serverUser@serverIP:[Path of Folder to be copied] .
	--This downloads everything present in the folder recursively into the current working directory
	scp test.txt serverUser@serverIP:[Path of Destination]
	--This uploads test.txt to the server
