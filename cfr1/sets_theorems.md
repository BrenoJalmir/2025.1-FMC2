```lean
θ.set_eq_eq := (∀A,B : Set α)(∀x : α)[(x ∈ A ⇔ x ∈ B) ⇔ A ⊆ B & B ⊆ A]
Sejam A, B : Set α.
Parte (∀A,B : Set α)(∀x : α)[(x ∈ A ⇔ x ∈ B) ⇒ A ⊆ B & B ⊆ A]
  Seja h : x ∈ A ⇔ x ∈ B (x ∈ A ⇒ x ∈ B ∧ x ∈ B ⇒ x ∈ A).
  Split.
  Parte L: -- A ⊆ B
    Seja x ∈ A.
    Logo x ∈ B [h·l].
  Parte R: -- B ⊆ A
    Seja x ∈ B.
    Logo x ∈ A [h·r].
Parte (∀A,B : Set α)(∀x : α)[A ⊆ B & B ⊆ A ⇒ (x ∈ A ⇔ x ∈ B)]
  Seja h : A ⊆ B & B ⊆ A.
  Split.
  Parte x ∈ A ⇒ x ∈ B:
    Seja x ∈ A.
    Logo x ∈ B [h·l; (⊆).1]
  Parte x ∈ B ⇒ x ∈ A:
    Seja x ∈ B.
    Logo x ∈ A [h·r; (⊆).1]
```