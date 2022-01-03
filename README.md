# Kotlin Numeric Matrix Processor
Proyecto de evaluación para el título de Kotlin Developer en Jetbrains Academy. Consiste en realizar una calculadora de matrices.

[![Kotlin](https://img.shields.io/badge/Code-Kotlin-blueviolet)](https://kotlinlang.org/)
[![LISENCE](https://img.shields.io/badge/Lisence-MIT-green)]()
![GitHub](https://img.shields.io/github/last-commit/joseluisgs/Kotlin-NumericMatrixProcessor)


![imagen](https://www.adesso-mobile.de/wp-content/uploads/2021/02/kotlin-einfu%CC%88hrung.jpg)

## Acerca de
Este proyecto de la academia Jetbrains fue realizado con el fin de evaluar la capacidad de desarrollo de Kotlin. consiste en ir haciendo un na calculadora de operaciones de matrices.

- [Kotlin Numeric Matrix Processor](#kotlin-numeric-matrix-processor)
  - [Acerca de](#acerca-de)
  - [Enunciado](#enunciado)
    - [Parte 1](#parte-1)
      - [Description: Matrix addition](#description-matrix-addition)
    - [Parte 2](#parte-2)
      - [Description: Multiplication by a scalar](#description-multiplication-by-a-scalar)
    - [Parte 3](#parte-3)
      - [Description: Matrix by matrix multiplication](#description-matrix-by-matrix-multiplication)
    - [Parte 4: Transpose](#parte-4-transpose)
      - [Description](#description)
    - [Parte 5: Determined!](#parte-5-determined)
      - [Description](#description-1)
    - [Parte 6: Inverse matrix](#parte-6-inverse-matrix)
      - [Description](#description-2)
  - [Autor](#autor)
    - [Contacto](#contacto)
  - [Licencia](#licencia)

## Enunciado
### Parte 1
#### Description: Matrix addition
Matrices have a wide range of applications in programming: they're used for digital image processing, graph representation and algorithms on a graph, graphic effects, applied math, statistics, and much more.

Since matrices are tables of numbers, they are usually presented in code as 2D-lists. In this project, you will learn how to read and output matrices, do operations on them, and compute the determinant of a square matrix. At first, you will work with matrices with integer elements, and later the elements will be floating-point numbers.

Let’s start with matrix addition.

For two matrices to be added, they must have an equal number of rows and columns. The sum of matrices AA and BB will be a matrix with the same number of rows and columns as AA or BB. The sum of AA and BB, denoted A + BA+B or B + AB+A, is computed by adding the corresponding elements of AA and BB: (A + B)_{n,m} = A_{n, m} + B_{n, m}(A+B) 


### Parte 2
#### Description: Multiplication by a scalar
In this stage, you are going to implement the multiplication of a matrix by a constant. To do this, you need to multiply every element of the matrix by that constant. 
Write a program that:
1. reads a matrix and a constant,
2. outputs the result of their multiplication.

### Parte 3
#### Description: Matrix by matrix multiplication
The next stage is the multiplication of matrices. This operation is a little more complex because it’s not enough to simply multiply the corresponding elements.

Unlike with addition, the sizes of the matrices can be different: the only restriction is that the number of columns in the first matrix should equal the number of rows for the second matrix. Check out a comprehensive video by 3Blue1Brown about matrix multiplication.

The multiplication of AA matrix with nn rows and mm columns and BB matrix with mm rows and kk columns is C_{n , k} = A_{n , m} \times B_{m, k}C 
n,k


The resulting matrix has nn rows and kk columns, where every element is a sum of the multiplication of mm elements across the rows of matrix AA by mm elements down the columns of matrix BB.

Another really important thing is that A_{i , j} \times B_{j , k}A i,j is not equal to B_{j, k} \times A_{i , j}B j,k ×A i,j. In fact, these are not even possible to multiply if k \ne i.k =i. If k = ik=i, the resulting matrices would still be different.

### Parte 4: Transpose
#### Description
In this stage, you should implement matrix transposition. Matrix transposition is an operation in linear algebra that replaces rows with columns and returns a new matrix as a result. This is an operation on just a single matrix.
In math, there is only one type of matrix transposition: transposition along the main diagonal. In this stage, you should implement the other three types of transposition to practice your list skills. These four types are:

- transposition along the main diagonal
- transposition along the side diagonal
- transposition along the vertical line
- transposition along the horizontal line


### Parte 5: Determined!
#### Description
In this stage, you should write a program that calculates a determinant of a matrix. You can check out some videos about linear algebra to understand the essence of the determinant and why it is important. To see how to calculate the determinant of any square matrix, watch a video about minors and cofactors and computing the nxn determinant. Also, here's nice graphic explanation on minors and cofactors.

### Parte 6: Inverse matrix
#### Description
In this stage, you should find the inverse of a matrix.

The inverse matrix A^{−1}A 
−1
  is the matrix whose product with the original matrix AA is equal to the identity matrix.

A \times A^{-1} = A^{-1} \times A = IA×A 
−1
 =A 
−1
 ×A=I

Watch a video about the inverse of a matrix to get the basic idea. To get a deeper understanding, check out the 3Blue1Brown channel.

The identity matrix is a matrix where all elements of the main diagonal are ones, and other elements are zeros. Here is an example of a 4, 44,4 identity matrix:


As you can see, it contains a lot of operations you implemented in the previous stages: finding cofactors of all the elements of the matrix, transposition of the matrix, finding the determinant of a matrix, and multiplication of a matrix by a constant.

det(A)det(A) is the determinant of matrix AA, and C^TC 
T
  is the matrix consisting of cofactors of all elements of the matrix AA transposed along the main diagonal. The inverse matrix can’t be found if det(A)det(A) equals zero. You can look up a calculation example.

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