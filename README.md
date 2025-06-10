# APP-6B
This project aims to simplify the integration of APP-6B symbology by supplying a JSON file that lists possible code combinations for easier retrieval and interpretation. Code examples will follow in a subsequent commit.

### From NATO JOINT SYMBOLOGY APP-6(B), ANNEX B – SYMBOL IDENTIFICATION CODING

1. **Code scheme (Position 1)**: This position indicates the overall symbology set to which a symbol belongs.
2. **Affiliation, battle dimension, and status (Positions 2-4)**: These positions determine the frame shape of a symbol and indicate its actual or planned location.
3. **Function ID (Positions 5-10)**: These positions identify a symbol’s function, with each position providing increasing levels of detail and specialization. The specific values for these positions are included with the symbol ID codes in Tables B-III through B-X.
4. **Size/mobility indicator code (Positions 11-12)**: These positions identify the size and mobility of a symbol. Table B-II contains the specific code values used in these positions.
5. **Country code (Positions 13-14)**: These positions identify the country with which a symbol is associated. Country code identifiers are listed in Federal Information Processing Standard (FIPS) Pub 10 series.
6. **Order of battle (Position 15)**: This position provides additional information about the role of a symbol in the battlespace. For example, a bomber that has nuclear weapons on board may be strategic force-related, or a tactical graphic may also perform the role of a control point.

**Symbol ID** Tables B-III through B-VIII list the codes for space, air, ground, sea surface, sea subsurface, and special operations symbols, respectively. Tables B-IX and B-X list the codes for tactical and weather graphics. In each table, an alphanumeric character indicates the known value for that position for a given symbol. An asterisk (*) indicates a position that is defined by the user based on specific symbol circumstances. A dash (-) indicates that no information is provided in the position. 

`CODING SCHEME (1) | AFFILIATION (1) | BATTLE DIMENSION (1) | STATUS (1) | FUNCTION ID (6) | SIZE/MOBILITY (2) | COUNTRY CODE (2) | ORDER OF BATTLE (1) 

---
The file structures the six fields as a list of objects. Each object contains a key for programmatic use and a descriptive name taken from the document's Annex B.

Example:
`
"CODING_SCHEME": [
		{
			"key": "S",
			"name": "WARFIGHTING"
		},
		{
			"key": "G",
			"name": "TACTICAL GRAPHICS"
		},
		{
			"key": "W",
			"name": "WEATHER"
		},
		{
			"key": "I",
			"name": "INTELLIGENCE"
		},
		{
			"key": "M",
			"name": "MAPPING"
		}
	],
`
