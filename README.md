# algo_project2

## DESCRIPTION

<!--PROBLEM 1-->

- Given two sets of elements, find the sum of all distinct elements from the set. In other words, find the sum of all elements which are present in either of the given set.
<!--PROBLEM 2-->
- Write a procedure, called dot_product which calculates in the variable ps, the dot(scalar) product of v1 and v2 (v1 and v2 are vectors of IR)
- Write an algorithm which determines, for n pairs of given vectors, whether two vectors of given IR are orthogonal, by calling the procedure defined in the previous question. The dot product of two orthogonal vectors is zero.

## ALGORITHM

### PROBLEM 1

Algorithm sum_distinct_elements <!--name of algo-->

Var: <!--variables-->
tab_1 :ARRAY_OF integer[4]; <!--first table-->
tab_2 :ARRAY_OF integer[4]; <!--second table-->
tab_3 :ARRAY_OF integer[8]; <!--third table, where we put the distinct elements-->
i, j, z, sum : integer; <!--i, j, z for for loop and sum to store the result-->

<!--THE BODY-->

BEGIN

<!--initialization-->

tab_1 :=[1, 2, 4, 8];
tab_2 :=[2, 3, 7, 5];
sum := o;

<!--elements of the first table -->

for(i from 0 to 3) do
for(j from 0 to 3) do
if(tab_1[i] == tab_2[j]) then <!--check if they re similar-->
break;
else <!--if not we enter the value of tab1 in tab3-->
for (z from 0 to tab_3.length-1) do
tab3[z] := tab1[i];
z := z + 1;
END_FOR
END_IF
END_FOR
END_FOR

<!--elements of the second table -->

for(j from 0 to 3) do
for(i from 0 to 3) do
if(tab_2[j] == tab_1[i]) then <!--check if they re similar-->
break;
else <!--if not we enter the value of tab2 in tab3-->
for (z from 0 to tab_3.length-1) do
tab3[z] := tab2[j];
z := z + 1;
END_FOR
END_IF
END_FOR
END_FOR

for(z from 0 to tab_3.length-1) do
sum := sum + tab_3[z]
END_FOR

### PROBLEM 2

<!-----LA PROCEDURE-------->

procedure dot_product(v, w, produit)
produit :=0; <!--le resultat du produit-->
for(i from 0 to 2 ) do
produit := produit + v(i) x w(i); <!--calcule le produit element par element et faire la somme-->
PRINT(produit);
END_FOR
END_PROCEDURE

<!-----ALGORITHM-------->

ALGORITHM check_orthogonality

var:
v: table_of integer[3];
w: table_of integer[3];
i : integer;
produit: integer;

BEGIN

<!--saisir les valeurs des vect par lutilisateur-->

for(i from 0 to 2 ) do
PRINT("Enter value for v[", i+1, "]: ");
READ(v(i));
PRINT("Enter value for w[", i+1, "]: ");
READ(w(i));
END_FOR

<!--calculer le produit scalaire-->

dot_product(v, w, produit);

<!--verifier l'orthogonalité-->

if (produit = 0)then
PRINT ("vectors are orthogonals");
else
PRINT ("vectors are not orthogonals");
END_IF
END
