# How to edit an ISO file

Sometimes, it necessary to edit ISO files, and this can be done as follows.

	cd /path/to/the/iso/file
	mkdir tmp
	sudo mount -o loop example.iso ./tmp

since iso is read only 
first make a copy of it
then modify copy

	cp -rvf tmp tmp_new

now do a modification

	touch tmp_new/readme.txt

and recreate the iso:

	sudo mkisofs -o example_new.iso tmp_new

that is it!

