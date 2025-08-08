# C# Classes

## Variables
Decimal     | append .m or .M at the number     | e.g.: dec num = 12.3M;
Float       | 
Int         | simply type the number            | e.g.: int num = 1;
String      | use double quotes                 | e.g.: string text = "simpletext";
Char        | use single quote                  | e.g.: char letter = 'a';

## String Formatting
\n -> skips one line
\t -> tab
\" -> double quotes
\\ -> backslash
\u -> unicode utf-16

### Verbatim
Keeps everything inside the double quotes except for double quotes, which need to be duplicated
``Console.Write(@"text\text\text""text""");``

#### Example:
```
Console.WriteLine("Generating invoices for customer \"Contoso Corp\" ...\n");
Console.WriteLine("Invoice: 1021\t\tComplete!");
Console.WriteLine("Invoice: 1022\t\tComplete!");
Console.WriteLine("\nOutput Directory:\t");
Console.Write(@"c:\invoices");
```

To generate Japanese invoices:
*Nihon no seikyū-sho o seisei suru ni wa*:

```Console.Write("\n\n\u65e5\u672c\u306e\u8acb\u6c42\u66f8\u3092\u751f\u6210\u3059\u308b\u306b\u306f\uff1a\n\t");```

User command to run an application
``Console.WriteLine(@"c:\invoices\app.exe -j");
``

**Output**:
```
Generating invoices for customer "Contoso Corp" ...

Invoice: 1021            Complete!
Invoice: 1022            Complete!

Output Directory:
c:\invoices

日本の請求書を生成するには：
    c:\invoices\app.exe -j
```

### Interpolation

Add '$' before the double quotes
```
var thing = "text";
Console.WriteLine($"this is a {thing}");
```

**Output**:

``this is a text;``

### Interpolation and Verbatim

add "$@" before the double quotes

```
var thing = "First-Project";
Console.WriteLine($@"C:\Output\{thing}\Data");
```
**Output**:

``C:\Output\First-Project\Data;``