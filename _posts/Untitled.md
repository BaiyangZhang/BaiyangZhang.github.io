---
layout: post
title: 
date: 
author: Baiyang Zhang
catalog: true
tags:
---

# Chapter 1

```mathematica
In[1]:= << "Quantum`Notation`";

In[2]:= SetQuantumAliases[]

Out[2]= "ALIASES:
[ESC]ket[ESC]        ket template
[ESC]bra[ESC]        bra template
[ESC]braket[ESC]     braket template
[ESC]op[ESC]         operator template
[ESC].[ESC]          quantum concatenation infix symbol
[ESC]on[ESC]         quantum concatenation infix symbol
[ESC]tp[ESC]         tensor product infix symbol
[ESC]qp[ESC]         quantum product template
[ESC]qs[ESC]         sigma notation for sums template
[ESC]si[ESC]         sigma notation for sums template
[ESC]ev[ESC]         eigenvalue-label template
[ESC]eket[ESC]       eigenstate template
[ESC]eeket[ESC]      two-operators-eigenstate template
[ESC]eeeket[ESC]     three-operators-eigentstate template
[ESC]ebra[ESC]       bra of eigenstate template
[ESC]eebra[ESC]      bra of two-operators-eigenstate template
[ESC]eeebra[ESC]     bra of three-operators-eigentstate template
[ESC]ebraket[ESC]    braket of eigenstates template
[ESC]eebraket[ESC]   braket of two-operators-eigenstates template
[ESC]eeebraket[ESC]  braket of three-operators-eigentstate template
[ESC]ketbra[ESC]     operator (matrix) element template
[ESC]eketbra[ESC]    operator (matrix) element template
[ESC]eeketbra[ESC]   operator (matrix) element template
[ESC]eeeketbra[ESC]  operator (matrix) element template
[ESC]her[ESC]        hermitian conjugate template
[ESC]con[ESC]        complex conjugate template
[ESC]norm[ESC]       quantum norm template
[ESC]trace[ESC]      partial trace template
[ESC]comm[ESC]       commutator template
[ESC]anti[ESC]       anticommutator template
[ESC]su[ESC]         subscript template
[ESC]po[ESC]         power template

The quantum concatenation infix symbol [ESC]on[ESC] is used for operator \
application, inner product and outer product.

SetQuantumAliases[] must be executed again in each new notebook that is \
created, only one time per notebook."

Declare  the  following symbols to be quantum operators. num is the number opreator, Ham the Hamiltonian.

In[3]:= SetQuantumObject[a, num, Ham]; 

Define  how  the  ladder  operators  act  on  the  eigenstates of Hamiltonian. Note that a and a^\[Dagger] need to be defined separately.
DefineOperatorOnKets[a,{\[VerticalSeparator]n_\[RightAngleBracket]:>Sqrt[n]\[VerticalSeparator](n-1)\[RightAngleBracket]}];
DefineOperatorOnKets[(a)^\[Dagger],{\[VerticalSeparator]n_\[RightAngleBracket]:>Sqrt[n+1]\[VerticalSeparator](n+1)\[RightAngleBracket]}];

Run some tests. Note that acting of operators on the states, inner products between states are done by dot products, the keyboard short key is esc+on+esc:

In[22]:= a\[CenterDot]\!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["3",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Out[22]= Sqrt[3] \!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["2",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

In[7]:= \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["3",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)\[CenterDot]SuperDagger[a]

Out[7]= Sqrt[3] \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["2",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

In[9]:= \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["b",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)\[CenterDot]SuperDagger[
\!\(\*OverscriptBox[\(a\), \(^\)]\)]

Out[9]= \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["b",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)\[CenterDot]SuperDagger[
\!\(\*OverscriptBox[\(a\), \(^\)]\)]

In[27]:= SuperDagger[a]\[CenterDot]\!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["3",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Out[27]= 2 \!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["4",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Define  the number operator:

In[28]:= num = SuperDagger[a]\[CenterDot]a;

In[29]:= num\[CenterDot]\!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["3",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Out[29]= 3 \!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["3",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

In[30]:= num\[CenterDot]\!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["m",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Out[30]= m \!\(\*
TagBox[
RowBox[{"\[VerticalSeparator]", 
TagBox["m",
Quantum`Notation`zz080KetArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[RightAngleBracket]"}],
Quantum`Notation`zz080Ket,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

In[31]:= \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["3",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)\[CenterDot]num

Out[31]= 3 \!\(\*
TagBox[
RowBox[{"\[LeftAngleBracket]", 
TagBox["3",
Quantum`Notation`zz080BraArgs,
BaseStyle->{ShowSyntaxStyles -> True},
Editable->True,
Selectable->True], "\[VerticalSeparator]"}],
Quantum`Notation`zz080Bra,
BaseStyle->{ShowSyntaxStyles -> False},
Editable->False,
Selectable->False]\)

Define the commutators:

In[32]:= \!\(\*
TagBox[
SubscriptBox[
RowBox[{"[[", 
TagBox[
RowBox[{"a", ",", 
SuperscriptBox["a", "\[Dagger]"]}],
Quantum`Notation`zz080KetArgs,
Editable->True,
Selectable->True], "]]"}], "-"],
Quantum`Notation`zz050Commutator,
Editable->False,
Selectable->False]\) = 1;
\!\(\*
TagBox[
SubscriptBox[
RowBox[{"[[", 
TagBox[
RowBox[{"N", ",", 
SuperscriptBox[
RowBox[{"(", "a", ")"}], "\[Dagger]"]}],
Quantum`Notation`zz080KetArgs,
Editable->True,
Selectable->True], "]]"}], "-"],
Quantum`Notation`zz050Commutator,
Editable->False,
Selectable->False]\) = SuperDagger[(a)];
\!\(\*
TagBox[
SubscriptBox[
RowBox[{"[[", 
TagBox[
RowBox[{"N", ",", "a"}],
Quantum`Notation`zz080KetArgs,
Editable->True,
Selectable->True], "]]"}], "-"],
Quantum`Notation`zz050Commutator,
Editable->False,
Selectable->False]\) = -a;

Define  the Hamiltonian operator in terms of x and p first, then convert it to a and a^\[Dagger].

Ham =
```