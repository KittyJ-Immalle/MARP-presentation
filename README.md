<!-- $theme: gaia -->

### Wat zijn optionele parameters?
*zie hoofdstuk 5.10*

Optionele parameters zijn parameters die al een standaardwaarde hebben en daarom **moeten** ze niet gebruikt worden.

---

**Optionele parameters (voorbeeld):**
```
static void Main(string[] args)
        {
            // Number already has a default value
            PrintTheNumber();
        }

        private static void PrintTheNumber(int number = 0)
        {
            Console.WriteLine("The number is " + number);
        }
```

---

### Wat is parameter-binding? 
*zie hoofdstuk 5.20*

**Parameter-binding (voorbeeld):**
```
static void Main(string[] args)
    	{
    	    int som, verschil;
            SomEnVerschil(15, 50, out som, out verschil);
        }

private static void SomEnVerschil(int getal1, int getal2, out int som, out int verschil)
        {
            som = getal1 + getal2;
            verschil = getal1 - getal2;
        }
```

---

### Wat is method-overloading?
*zie hoofdstuk 5.22*

Een method kan meerdere overloads hebben. Overloading gebeurt wanneer je twee methods met **dezelfde** naam hebt maar met verschillende parameters. Bij het compilen, gaat de compiler kiezen welke method hij moet gebruiken.

---

**Method overloading (voorbeeld):**
```
private void Swap(ref int a, ref int b)
        {
            int temp;
            temp = a;
            a = b;
            b = temp;
        }
        private void Swap(ref double a, ref double b)
        {
            double temp;
            temp = a;
            a = b;
            b = temp;
        }
```

---

### Hoe herken je in WPF event-handlers? 
*zie ook hoofdstuk 5.10*

Event-handlers zijn speciale methods die een *event handlen*. Ze wachten op een bepaalde event, en voeren de method uit als deze event zich voordoet.
**Event-handlers (voorbeeld):**
```
private void button_Click(object sender, RoutedEventArgs e)
        {
            label.Content = textBox.Text;
        }
```

---

### Waar moet je op letten bij b.v. de `AddYears()`-method van een `DateTime`-object?

`AddYears()` *returnt* enkel een datum. Je moet nog iets met deze waarde doen.
```
DateTime time = new DateTime();
            time = time.AddYears(2);
            /* This is wrong:
             * time.AddYears(2);
             */
```

---

### Als je een variabele niet initialiseert welke waarde heeft hij dan?

Dit hangt altijd af van het type.

---

**Value types**

*voorbeelden:*

bool:	false

byte:	0

char:	'\0'

decimal:	0M

double:	0.0D

float:	0.0F

---

int:	0

long:	0L

sbyte:	0

short:	0

uint:	0

ulong:	0

ushort:	0

---

**Reference types**

*voorbeelden:*

String

objecten

arrays

lists

Random



