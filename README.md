# tema-1.2

Citeste de la tastatura un numar x
- afiseaza pe ecran suma cifrelor sale.
- daca toate cifrele sale sunt pare, afiseaza un mesaj care sa arate asta
- afiseaza numarul cifrelor pare si impare ale lui x 
- afiseaza suma cifrelor pare si suma cifrelor impare 
- afiseaza daca numarul este palindrom* sau nu (palindrom = citind cifrele sale de la dreapta la stânga se obţine acelaşi număr ex 12321)


X=input("Numarul este:")
Lungime=len(X)
i=0
Suma=0
CountPar=0
SumPar=0
CountImpar=0
SumImpar=0
while i<Lungime:
    if int(X[i]) % 2 ==0:
        CountPar+=1
        SumPar+=int(X[i])
    else:
        CountImpar+=1
        SumImpar+=int(X[i])
    Suma+=int(X[i])
    i+=1
print("Suma cifrelor numarului {0} este {1}".format(X,Suma))
if CountPar==Lungime:
    print("Toate cifrele numarului {0} sunt pare".format(X))
else:
    print("Numarul {0} are {1} cifre pare si {2} cifre impare".format(X,CountPar,CountImpar))
    print("Pentru numarul {0} suma cifrelor pare este {1}, iar suma cifrelor impare este {2}".format(X,SumPar,SumImpar))
Y=X[::-1]
if X==Y:
    print("Numarul {0} este palindrom".format(X))
else:
    print("Numarul {0} nu este palindrom".format(X))




Citeste de la tastatura numere pana se citeste valoarea 0. apoi:
- Sa se afiseze cel mai mare numar citit de la tastatura 
- Sa se afiseze suma numerelor impare citite
- Sa se afiseze numarul maxim de numere citite consecutiv crescator 
(exemplu:
1 2 3 0 -> 3 numere (1 2 3)
1 2 0 3 4 5 -> 3 numere (3 4 5)
5 3 2 0 -> 0 numere 
5 3 1 2 -> 2 numere (1 2)
)


X=input("Numarul este: ")
Max=int(X)
Cons=int(X)
SumImpar=0
CountInc=0
while int(X)!=0:
    if Max<int(X):
        Max=int(X)
        if int(X) % 2!=0:
            SumImpar+=int(X)
    else:
        if int(X) % 2!=0:
            SumImpar+=int(X)
    if Cons+1==int(X):
        CountInc+=1
    else:
        CountInc=1
    Cons=int(X)
    X=input("Urmatorul numar este: ")
print("Cel mai mare numar citit de la tastatura este {0} ".format(Max))
print("Suma numerelor impare citite de la tastatura este {0}".format(SumImpar))
print("Numarul maxim de numere citite consecutiv este {0}".format(CountInc))
