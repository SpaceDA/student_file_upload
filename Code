	# This short script was designed to upload my student performance reports to individual student folders. All files were named in the same manner: 
	# Group_2-Digit Grad Year_LASTNAME.pdf (ex. MOC_22_SMITH.pdf). Adjust the regex expression if your files are named differently. 
	import os
	import re
	import shutil
	
	
	source = input('What is the full path of the source folder?)
	#gives all files in source folder in a list format.
	lst_source = os.listdir(source)
	
	dest = input('What is the full path of the destination?)
	#use regular expressions to tell the program where to look in the file name. For me, it was the LASTNAME.
	pattern = '[0-9]_(A-Z)+'
	
	#loops through each file in source, extracting the "LASTNAME" - which I used to direct the file to the correct student folder. If your folders are named differently, you'll have to adjust. 
	for file in lst_source:
		name = re.findall(pattern, file)
		shutil.move(source + '/' + str(file), dest + "/".join(name))
	
