# README
The file ```charDecl.xml``` contains all entries from ```charlist.org``` as tei. 
The ```charDecl``` element shoudl be inculded in the ```profilDesc``` inside the ```teiHeader```.
Depending on default font settings you might see Tofu's within the file. This is a font problem, the proper characters are encoded!
   
## CHANGES:
* The @IDs are computed via ```gaiji_unicode.xql```.
    * It takes value of ```@type="Unicode"``` as default, and ```@type="standard"``` as fallback.
    * ```@n``` contains the original ID scheme.
* Characters without unicode representation are transcribed in Unicode IDC format. 
    * If component variants are available under unicode these are used instead of unihan equivalents: 
        * 汄 = ```⿰氵人``` (U+6C35)  instead of ```~~⿰水人~~``` (U+6C35).
        * 说 = ```⿰讠兑``` (U+8BA0) instead of ```~~⿰言兌~~``` (U+8A00).
    * These glyphs keep the original ID as xml:ID.
