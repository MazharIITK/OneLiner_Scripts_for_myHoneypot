# Lits of one liner bash scripts which will help to explore my Honeypot:

1) To count the number of different IPs which attacked my Honeypot
	
	$:~ _echo */ | wc_


2) To list all directories which have attacked my Honeypots 'n' number of times. (Put any value in place of 'n')

	
	$:~ _find . -maxdepth 1 -type d -exec bash -c "echo -ne '{} '; ls '{}' | wc -l" \; | >  awk '$NF>=1000'_
	
	
	Note: Here, I have put n = 1000, you can put any value of 'n' of your choice.
