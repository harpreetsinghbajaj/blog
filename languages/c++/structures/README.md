Variable length structures

 Those which have an array of undefined size at the compile time.
typedef struct var_length_s {
    int age;
    char emp_name[];
} var_len_t;

If you create a stack variable of the above structure and use the emp_name then the compile time error will be generated
The following is the way to use the above structure:à
var_len_t *var2 = NULL;
var2 = (var_len_t*)malloc(sizeof(var_len_t) + 100*sizeof(char));
strncpy(var2->emp_name, "Harpreet Singh Bajaj", 100);

This type of structure is used a lot in the network programming because the header can be freezed but the size of data that need to be
send can be calculated and allocated at run time.

 Structure padding
It is about facilitating the reading of elements in the structure in one read. On a 4 byte word boundary system, one read reads 4 bytes and on a
8 byte word boundary system, one read reads 8 bytes.

So on a 8 byte word boundary system,
sizeof following structure is 32 bytes
struct X
{
int p;
struct X *y;
char z;
char *b;
};
This is because once the int occupies the 4 bytes, the next pointer need 8 bytes.
If 4 bytes are stored after int and 4 bytes are stored in the next word, two reads are required.

size of following structure is 24 bytes because the above case it not happening in this.
struct X
{
struct X *y;
int p;
char z;
char *b;
};

