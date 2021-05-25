# Linux-Basics
commands to practice:
1.pwd present working directory

# pwd 

2. whoami by using this command we can trace the current logged in user

# whoami

3.cat we can use cat command in 3 ways
  a)	Inorder to see the content in the cat command use the following syntax
   	# cat filename
   	eg:cat dharma
  b)	For creating the file with cat command use the following command
  	# cat > filename
	eg:cat > dharma
	once we have given the above command it will prompt for entering the content to the file. once done with the content for save and exit the file use ctrl+c
	NOTE: if the file was already exists with the content we will loose the  content if we use the above command.
  c)	Inorder to append the content in the specific file with cat command use the following syntax
	#  cat >> filename
	eg: cat >> dharma
  	once we have given the above command it will prompt for entering the content to the file. once done with the content for save and exit the file use ctrl+c

4. mkdir by using this command we can create empty directories.use the following syntax
	# mkdir directoryname 
	eg: mkdir siraparapu


   we can also create the nested files by using the following syntax.
	# mkdir -p dir1/dir2/dir3
	eg: mkdir -p sir1/sir2/sir3


5. rmdir by using this command we can delete the empty directories.use the following syntax
	# rmdir directoryname
	eg: rmdir siraparapu


   we can also delete the directory recursively by using the following syntax.
	# rm -rf dir1/dir2/dir3
	eg: rm -rf sir1/sir2/sir3


6. cp by using this command we can copy from source to destination 
	# cp -r source destination
	eg:cp -r /opt/aly /dharma


7. touch by using this command we can create the empty files
	# touch filename
	eg: touch dharma
	inorder to create the multiple files use the following syntax
	# touch filename filename filename
	eg: touch d1 d2 d3 


8. ls by using the following commands we can list the files and folders
 	ls in order to see the files and folders in the required path
	ls -l to display all the information about files and folders 
	ls -a to display all the information about files and folders including hidden files
	ls -1 to display all the information in the pattern of one file per line
	ls -R to display all the recursive files and folders
	ls -lt to display the files according to the last modified time
	ls -ltr to display the files according to the last modified time in the reverse order
	ls -i to display files and folders with inode number


9. move by using this command we can move from source to destination
	# mv source destination
	eg: mv /etc/alekhya /opt/dharma


10.cd  by using this command we can change the directories from one to another
	# cd directoryname
	eg: cd dharma
 	cd inorder to go to the directory to the loggedin user
	# cd


11. find by using this command we can find the files under the current tree
 	# find . -name '*.js'
	eg: find . -name '*.txt'
	inorder to find the directories under the current tree having the name dharma
	# find . type d -name dharma
	eg: find . type d -name dharma
	for case sensitive we can replace name with iname
	we can find under multiple roots 
	# find folder1 folder2 -name filename.txt
	eg: find dhar aly -name r2.txt
	To find directories under current tree matching dharmadharma
	# find . -type d name dharmadharma
	we can exclude the path using -not -path
	# find . -type d name '*.js' -not -path 'directory name'
	eg: find . -type d name '*.txt' -not -path 'dharma'
	we can find the files having more than 1000kb
	# find . -type f -size +100kb
	eg: find . -type f -size +100kb
	we can find tye files having the size greater than 10kb and less than 20kb
	# find . -type f -size +10kb -size 500kb
	eg: find . -type f -size +10kb -size 500kb
	to find the files edited more than 3 days
	# find . -type f mtime +3
	eg: find . - type f mtime +3
	to find the files edited last 1 day
	# find . -type f mtime -1
	we can delete the files edited in the last 1 day by adding the command -delete
	# find . -type f mtime -1 -delete

12.grep 
	grep stands for global regular expression print
	consider the demofile having some content
	#grep 'searchword' filename
	eg: grep 'dharma' filename
	for searching in multiple files
	# grep "dharma" demo1 demo2
`	for case sensitive add -i
	for finding the line starting with some word and ending with some word
	# grep "line .*end" demofile
	inorder to finding the files recursively
	grep -r "dharma"
	for finding the lines without the word searched add -v
	#grep -v "word"
	eg: grep -v "dharma"
	for counting the searched words
	# grep -c "filename"
	eg: grep -c "dharma"
	matching all the lines having the latters a,b,c,d,e
	grep "[a-e]" filename
	matching the lines starting with the word ****
	grep "^hello" filename
	matching the line ending with the word ****
	grep "hello$" filename
	matching all the lines that not having vowel
	grep "[^vowel]" filename
	

13.gzip
	this command is used for compressing the files
	heres the simplest usage
	gzip "filename"
	by using the above command it compresses and deletes the original file
	gzip -k "filename"
	there are various levels of compressions in the range 0-9 .the more the number the more delay it takes
	gzip -1 "filename"
	and the default is 6
	we can compress the multiple files
	gzip filename1 filename2
	we can compress all the files in te directory by using -r
	gzip -r filename
	we can know the compressed percentage by adding -kv
	gzip -kv filename
	we can also decompress the file by using -d and ading .gz to the filename
	gzip -d filename.gz


14.gunzip
	by default -d is present in the gunzip command
	gunzip filename.gz
	we can extract into the other filename using -c command
	gunzip -c filename.gz > another file name
15.filter commands
	filter commands are used to filter the output so that required things can be easily picked up
	the commands used are
	less
	it is used to see the output pagewise or linewise
	less/etc/passwd
	more
	same as less command
	more/etc/passwd
	head
	inorder to display the top 10 lines of the file
	head/etc/passwd
	for top 5 lines
	head -n/etc/passwd , where n=5
	sort
	we can sort the file by using the following command
	sord filename
	we can reverse the order by using -r in the command
	sort -r filename
	we can remove the duplicate lines by using -u
	sort -u filename
	to sort file according to numbers use -d or -h
	sort -h filename
	cut
	cut command is used to make the sentence into te columns by adding -d -f
	cut -d -f filename
	to delimit i.e brining into the oroginal position use -d,-f1
	cut -d,-f1 filename
	sed command 
	this command is used for replace the word with the wanted word in the output
	note: it wont replace in the original file
	sed 's/replacable word/word/g' filename
	









