# cyber-security
bandit0 - how to use ssh:
	-p flag changes port
	format-> ssh FLAG FLAG_PARAMETER username@server

bandit0-1 - cat a README

bandit1-2 - dashed file:
	Use < to read dashed file with cat
	i.e cat < -filename

bandit2-3 - spaces in filename:
	Just put '' around the filename
	i.e cat 'file name with spaces'
	
bandit3-4 - Hidden files:
	I think they start in a .
	Use ls with -l or -a flag to see them

bandit4-5 - find human readable file:
	use find with -readable flag which checks for binary strings

bandit5-6 - find non executable files and files of a certain byte len:
	for non executable - 
		before putting the executable flag use ! to invert
		find ! -executable
	for certain byte len - 
		use size flag and pass the number of bytes followed by c
		find - size 33c

bandit6-7 - Find file owned by a user and/or group:
	User - 
		find -user username
	Group - 
		find -group groupname

bandit7-8 - Find a word in the same line as another word:
	grep "word you have" filename

bandit8-9 - find a unique line of text within a file:
	use sort and pipe uniq with the -u flag to only display unique lines
	sort filname | uniq -u

bandit9-10 - find a human readable string within the file:
	use strings command!
	strings filename

bandit10-11 - base64 decode
	base64 -d filename

bandit11-12 - rotate characters in file
	command is 'tr'
	its kinda weird, format goes
	cat data.txt | tr '[a-z]' '[letter that goes to a-za-letter before the letter that goes to a]'
	can pipe tr multiple times to catch more 
	reverse the format to decode/undo shift
