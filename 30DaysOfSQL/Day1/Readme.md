
QUERY #1 - Remove Redundant Pairs									
	"Problem Statement:
- For pairs of brands in the same year (e.g. apple/samsung/2020 and samsung/apple/2020) 
      - if custom1 = custom3 and custom2 = custom4 : then keep only one pair
- For pairs of brands in the same year 
      - if custom1 != custom3 OR custom2 != custom4 : then keep both pairs
- For brands that do not have pairs in the same year : keep those rows as well"								
									
									
									
									
									
									
	INPUT								
	BRAND1	BRAND2	YEAR	CUSTOM1	CUSTOM2	CUSTOM3	CUSTOM4		
	apple	samsung	2020	1	2	1	2		
	samsung	apple	2020	1	2	1	2		
	apple	samsung	2021	1	2	5	3		
	samsung	apple	2021	5	3	1	2		
	google		2020	5	9				
	oneplus	nothing	2020	5	9	6	3		
									
	OUTPUT								
	BRAND1	BRAND2	YEAR	CUSTOM1	CUSTOM2	CUSTOM3	CUSTOM4		
	apple	samsung	2020	1	2	1	2		
	apple	samsung	2021	1	2	5	3		
	samsung	apple	2021	5	3	1	2		
	oneplus	nothing	2020	5	9	6	3		
	google		2020	5	9				
