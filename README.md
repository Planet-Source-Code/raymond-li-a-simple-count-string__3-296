<div align="center">

## A Simple Count String


</div>

### Description

Aims to count how many words in the infile
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Raymond Li](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/raymond-li.md)
**Level**          |Beginner
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |C
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/raymond-li-a-simple-count-string__3-296/archive/master.zip)





### Source Code

```
/*****************************************/
/* Program Name : A Simple Count String */
/* Description : Aims to count how many */
/*        words in the infile  */
/* Programmer  : Raymond Li    	 */
/*****************************************/
#include <stdio.h>
#include <stdlib.h>
#define MAX_LENGTH 256
main(int argc, char *argv[])
{
 char inword[MAX_LENGTH];
 int word_count = 0;
 FILE *infile;
 if (argc < 2)
 {
 printf("Format : wordcnt <filename>\n");
 exit( 1 );
 }
 /* open the infile */
 if ((infile = fopen( argv[1], "rt" )) == NULL)
 {
 printf("Cannot open input file - %s\n", argv[1] );
 exit( 1 );
 }
 /* read the string and count it while not end of file */
 while( !feof(infile) )
 {
 fscanf( infile, "%s", inword );
 word_count++;
 }
 /* print the result */
 printf( "There are %d word(s) in the file %s\n", word_count, argv[1] );
 /* close the infile */
 fclose(infile);
 return(0);
}
```

