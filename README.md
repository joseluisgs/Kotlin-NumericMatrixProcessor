# Kotlin Simple Search Engine
Proyecto de evaluación para el título de Kotlin Developer en Jetbrains Academy. Consiste en realizar un buscador con distintas opciones e índice invertido.

[![Kotlin](https://img.shields.io/badge/Code-Kotlin-blueviolet)](https://kotlinlang.org/)
[![LISENCE](https://img.shields.io/badge/Lisence-MIT-green)]()
![GitHub](https://img.shields.io/github/last-commit/joseluisgs/Kotlin-SimpleSearchEngine)


![imagen](https://www.adesso-mobile.de/wp-content/uploads/2021/02/kotlin-einfu%CC%88hrung.jpg)

## Acerca de
Este proyecto de la academia Jetbrains fue realizado con el fin de evaluar la capacidad de desarrollo de Kotlin. consiste en ir haciendo un buscador de datos en un fichero con distintas opciones e indice inverso usando mapas, asi como parámetros de búsqueda.

- [Kotlin Simple Search Engine](#kotlin-simple-search-engine)
  - [Acerca de](#acerca-de)
  - [Enunciado](#enunciado)
    - [Parte 1](#parte-1)
      - [Description](#description)
      - [Objectives](#objectives)
      - [Examples](#examples)
    - [Parte 2](#parte-2)
      - [Description](#description-1)
      - [Objectives](#objectives-1)
      - [Example](#example)
    - [Parte 3](#parte-3)
      - [Description](#description-2)
      - [Objectives](#objectives-2)
      - [Example](#example-1)
    - [Parte 4](#parte-4)
      - [Description](#description-3)
      - [Objectives](#objectives-3)
      - [Example](#example-2)
    - [Parte 5](#parte-5)
      - [Description](#description-4)
      - [Objectives](#objectives-4)
      - [Example](#example-3)
    - [Parte 6](#parte-6)
      - [Description](#description-5)
      - [Objectives](#objectives-5)
      - [Example](#example-4)
  - [Autor](#autor)
    - [Contacto](#contacto)
  - [Licencia](#licencia)

## Enunciado
### Parte 1
#### Description
Let's implement the simplest search engine possible ever. It should search for a specific word in a multi-word input line.

The input line contains several words separated by a space. The words are numbered according to their order, with the first word having index 1. Consider that all the words in the line are unique, so there can be no repetition.

#### Objectives
Write a simple program that reads two lines: a line of words and a line containing the search word. The program must search in the first line for a word specified in the second one. The program should output the index of the specified word. If there is no such word in the first line, the program should print Not Found. Please remember that indexes start from 1!

You should output exactly one line.

#### Examples
The lines that start with > represent the user input. Note that these symbols are not part of the input.

Example 1:

```
> first second third fourth
> third
3
Example 2:

> cat dog and mouse
> elephant
Not found
> 
> 
```
### Parte 2
#### Description
Now, let's make our search a little more complex. Let's write a program that performs multiple searches in multiple text lines.

#### Objectives
Write a program that reads text lines from the standard input and processes single-word queries. The program must output all lines that contain the string from the query.

You may choose what kind of text you will input in your project. For example, each line may describe:

a person represented by the first name, the last name, and optionally an email;

an address of a building represented by the country, city, state, street, and zip code;

a book represented by its ISBN, title, author/authors, publisher, and so on.

You can use any of these options or come up with your own, but it is important to stick to the same type of data in your dataset throughout all stages of the project. As item delimiters, you can use spaces, commas (see CSV), or any other characters.

Here is an example of an input line. It contains three items: the first name, the last name, and an email address.

Elsa Sanders elsa@gmail.com
In this example, all items are separated by spaces.

The search should be case insensitive and ignore all extra spaces.

First, the user should input a number N, which is the number of data lines they are going to enter next. Then the user enters N lines with data. After that, the user enters a number M, which is the number of search queries. After each query, the program should print the information it managed to find among the data. You can see this searching process in the example below.

#### Example
In the following example, we use several names and e-mails as a dataset. The lines that start with > represent the user input. Note that these symbols are not part of the input.

Enter the number of people:
````
> 6
Enter all people:
> Dwight Joseph djo@gmail.com
> Rene Webb webb@gmail.com
> Katie Jacobs
> Erick Harrington harrington@gmail.com
> Myrtle Medina
> Erick Burgess

Enter the number of search queries:
> 3

Enter data to search people:
> ERICK

People found:
Erick Harrington harrington@gmail.com
Erick Burgess

Enter data to search people:
> unknown
No matching people found.

Enter data to search people:
> WEBB@gmail.com

People found:
Rene Webb webb@gmail.com
````
### Parte 3
#### Description
Let's modify the previously written search program an add a user menu for a better user experience.

#### Objectives
In this stage, you need to create a menu. The menu should display the following options:
```
1. Search information.
2. Print all data.
0. Exit.
```
   The user must select a menu item and then enter data if necessary. Your program must not stop until the corresponding option (exit) is chosen.

Decompose the program into separate methods to make it easy to understand and to further develop or edit.

#### Example
In the example below, we use people's names and emails as a dataset example. The lines that start with > represent the user input. Note that these symbols are not part of the input.
```
Enter the number of people:
> 6
Enter all people:
> Dwight Joseph djo@gmail.com
> Rene Webb webb@gmail.com
> Katie Jacobs
> Erick Harrington harrington@gmail.com
> Myrtle Medina
> Erick Burgess

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 3

Incorrect option! Try again.

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 1

Enter a name or email to search all suitable people.
> KATIE
Katie Jacobs

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 2

=== List of people ===
Dwight Joseph djo@gmail.com
Rene Webb webb@gmail.com
Katie Jacobs
Erick Harrington harrington@gmail.com
Myrtle Medina
Erick Burgess

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 0

Bye!
```

### Parte 4
#### Description
Now, let's further modify the program and teach it to read the input data from a file.

#### Objectives
In this stage, your program should read data from a text file instead of the standard input. The file structure will depend on your text data type (personal information, address information, book information, and so on). See an example below:
````
Dwight Joseph djo@gmail.com
Rene Webb webb@gmail.com
Katie Jacobs
Erick Harrington harrington@gmail.com
Myrtle Medina
Erick Burgess
````
The program must process the command line argument --data followed by the name of the file with the data, for example, --data text.txt.

Note that the file should not include the total number of lines. All lines must be read only once, at the start of your program.

#### Example
Here is an example of an output line, which contains three items: the first name, the last name, and an email address.

The lines that start with > represent the user input. Note that these symbols are not part of the input.
````
=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 1

Enter a name or email to search all matching people.
> WEBB@gmail.com
Rene Webb webb@gmail.com

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 0

Bye!
````
### Parte 5
#### Description
Now your program can successfully search for all matching lines, and the search is case- and space-insensitive. There is one problem though: you need to check each line to find out whether it contains the query string.

To optimize your program, you can use a data structure called an Inverted Index. It maps each word to all positions/lines/documents in which the word occurs. As a result, when we receive a query, we can immediately find the answer without any comparisons.

#### Objectives
In this stage, build an inverted index at the start of the program and then use the index for searching operations. You can implement it using the Map class. It connects an item with a list (or set) of indexes belonging to the lines that contain the item.

Suppose you have the following list of lines:
````
0: Katie Jacobs
1: Erick Harrington harrington@gmail.com
2: Myrtle Medina
3: Erick Burgess
````

For these lines, the inverted index will look like this:
````
Katie -> [0]
Jacobs -> [0]
Erick -> [1, 3]
Harrington -> [1]
harrington@gmail.com -> [1]
Myrtle -> [2]
Medina -> [2]
Burgess -> [3]
````
The order of pairs is not important. If you are searching for Erick, you can immediately get the target fields using this mapping.

Note that the Inverted Index is not intended to search for parts of a word, it is only used to search for full words.

#### Example
The lines that start with > represent the user input. Note that these symbols are not part of the input.
````
=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 1

Enter a name or email to search all matching people.
> ERICK
2 persons found:
Erick Harrington harrington@gmail.com
Erick Burgess

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 1

Enter a name or email to search all matching people.
> ROY@gmail.com
1 person found:
Richard    Roy    roy@gmail.com

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 1

Enter a name or email to search all matching people.
> john
No matching people found.

=== Menu ===
1. Find a person
2. Print all people
0. Exit
> 0

Bye!
````
### Parte 6
#### Description
Now let's Improve your search engine to make it support complex queries containing word sequences and use several strategies that determine how to match data.

#### Objectives
In this stage, your program should be able to use such searching strategies as ALL, ANY, and NONE.

Take, for example, these six sample lines:
````
Dwight Joseph djo@gmail.com
Rene Webb webb@gmail.com
Katie Jacobs
Erick Harrington harrington@gmail.com
Myrtle Medina
Erick Burgess
````
If the strategy is ALL, the program should print the lines containing all the words from the query.
````
Query:

Harrington Erick
Result:

Erick Harrington harrington@gmail.com
````
If the strategy is ANY, the program should print the lines containing at least one word from the query.
````
Query:

Erick Dwight webb@gmail.com
Result:

Erick Harrington harrington@gmail.com
Erick Burgess
Dwight Joseph djo@gmail.com
Rene Webb webb@gmail.com
````
If the strategy is NONE, the program should print the lines that do not contain any words from the query at all.
````
Query:

djo@gmail.com ERICK
Result:

Katie Jacobs
Myrtle Medina
Rene Webb webb@gmail.com
````
All the listed operations should be implemented with an inverted index, and the results should not contain any duplicates.

Do not forget to use methods to decompose your program.

#### Example
The lines that start with > represent the user input. Note that these symbols are not part of the input.
````
=== Menu ===
1. Find a person
2. Print all persons
0. Exit
> 1

Select a matching strategy: ALL, ANY, NONE
> ANY

Enter a name or email to search all matching people.
> Katie Erick QQQ

3 persons found:
Katie Jacobs
Erick Harrington harrington@gmail.com
Erick Burgess
````

## Autor

Codificado con :sparkling_heart: por [José Luis González Sánchez](https://twitter.com/joseluisgonsan)

[![Twitter](https://img.shields.io/twitter/follow/joseluisgonsan?style=social)](https://twitter.com/joseluisgonsan)
[![GitHub](https://img.shields.io/github/followers/joseluisgs?style=social)](https://github.com/joseluisgs)

### Contacto
<p>
  Cualquier cosa que necesites házmelo saber por si puedo ayudarte 💬.
</p>
<p>
    <a href="https://twitter.com/joseluisgonsan" target="_blank">
        <img src="https://i.imgur.com/U4Uiaef.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://github.com/joseluisgs" target="_blank">
        <img src="https://cdn.iconscout.com/icon/free/png-256/github-153-675523.png" 
    height="30">
    </a> &nbsp;&nbsp;
    <a href="https://www.linkedin.com/in/joseluisgonsan" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/768px-LinkedIn_logo_initials.png" 
    height="30">
    </a>  &nbsp;&nbsp;
    <a href="https://joseluisgs.github.io/" target="_blank">
        <img src="https://joseluisgs.github.io/favicon.png" 
    height="30">
    </a>
</p>


## Licencia

Este proyecto está licenciado bajo licencia **MIT**, si desea saber más, visite el fichero [LICENSE](./LICENSE) para su uso docente y educativo.