```lean
Set : * → *

(∈) : α × Set α → Prop

(⊆) : Set α ⨯ Set α → Prop
A ⊆ B ⇐≝⇒ (∀x ∈ A)[x ∈ B]

(∪) : Set α ⨯ Set α → Set α
x ∈ A ∪ B ⇐≝⇒ x ∈ A ∨ x ∈ B

(∩) : Set α ⨯ Set α → Set α
x ∈ A ∩ B ⇐≝⇒ x ∈ A ∧ x ∈ B

(∖) : Set α ⨯ Set α → Set α
x ∈ A ∖ B ⇐≝⇒ x ∈ A ∧ x ∉ B

(∆) : Set α ⨯ Set α → Set α
x ∈ A ∆ B ⇐≝⇒ x ∈ A ∪ B ∧ x ∉ A ∩ B

𝓅 : Set α → Set (Set α)
B ∈ (𝓅 A) ⇐≝⇒ B ⊆ A

(⋃) : Set (Set x) → Set α
x ∈ (⋃ A) ⇐≝⇒ {x : α | ∃B ∈ A, x ∈ B} ⇐≝⇒ (∃B)[B ∈ A & x ∈ B]

(⋂) : Set (Set α) → Set α
x ∈ (⋂ A) ⇐≝⇒ {x : α | ∀B ∈ A, x ∈ B} ⇐≝⇒ (∀B)[B ∈ A ⇒ x ∈ B]

Empty : Set α → Prop
Empty A ⇐≝⇒ (∀x:α)[x ∉ A]

Singleton : Set α → Prop
Singleton A ⇐≝⇒ (∃! x : α)[x ∈ A]

Subsingleton : Set α → Prop
Subsingleton A ⇐≝⇒ (∀u,v ∈ A)[u = v]

Universal : Set α → Prop
Universal A ⇐≝⇒ (∀x : α)[x ∈ A]
```