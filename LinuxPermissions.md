Viewing Permissions
	ls -l

Changing Permissions (chmod)
	+ -> add
	- -> remove
	= -> set

	Example: chmod a+r test.txt

Permissions with Respective Numerical values:
	4 = r
	2 = w
	1 = x
	0 = -

	Example: chmod 644 test.txt

Changing Ownership (chown & chgrp)
	chown (Change Owner):
		sudo chown testUser test.txt
	chgrp (Change Group):
		sudo chgrp testGroup test.txt

The -R Flag (Recursive)
	chmod -R 755 /testFolder
	--This modifies the permissions of everything present in the testFolder directory for user to have rwx and groups & others to have rx only
