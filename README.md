# Adjective Declension in Russian

## Introduction

In this project, I am trying to model adjective declension in Russian. The Russian language has a highly inflectional morphology, particularly in nouns, pronouns, adjectives (they are called nomials). In Russian, nominal declension involves six **cases** (nominative, genitive, dative, accusative, instrumental, and prepositional), two **numbers** (singular and plural), and **grammatical gender** (masculine, feminine, and neuter). To better illustrate the idea, a chart is provided below. The word "boy" is masculine, "girl" is feminine and "tree" is neuter.

### Singular Nouns

| Cases         | мальчик (boy)    | девочка (girl)  | древо (tree)  |
| ------------- | ---------------  | --------------  | ------------  |
| nominative    | мальчик          | девочк ***а***  | древ ***о***  |
| genitive      | мальчик ***а***  | девочк ***и***  | древ ***а***  |
| dative        | мальчик ***у***  | девочк ***е***  | древ ***у***  |
| accusative    | мальчик ***а***  | девочк ***у***  | древ ***о***  |
| instrumental  | мальчик ***ом*** | девочк ***ой*** | древ ***ом*** |
| prepositional | мальчик ***е***  | девочк ***е***  | древ ***е***  |

### Plural Nouns

| Cases         | мальчик (boy)     | девочка (girl)   | древо (tree)     |
| ------------- | ----------------  | ---------------  | ---------------  |
| nominative    | мальчик ***и***   | девочк ***и***   | древ ***еса***   |
| genitive      | мальчик ***ов***  | девочек          | древ ***ес***    |
| dative        | мальчик ***ам***  | девочк ***ам***  | древ ***есам***  |
| accusative    | мальчик ***ов***  | девочек          | древ ***еса***   |
| instrumental  | мальчик ***ами*** | девочк ***ами*** | древ ***есами*** |
| prepositional | мальчик ***ах***  | девочк ***ах***  | древ ***есах***  |

An adjective is generally placed before the noun it describes, and it must match the **case**, **number** and **gender** of the noun.

### Adjectives

| Cases                | masculine        | feminine        | neuter           | plural           |
| -------------------- | ---------------  | --------------  | ---------------  | ---------------  |
| nominative           | красив ***ый***  | красив ***ая*** | красив ***ое***  | красив ***ые***  |
| genitive             | красив ***ого*** | красив ***ой*** | красив ***ого*** | красив ***ых***  |
| dative               | красив ***ому*** | красив ***ой*** | красив ***ому*** | красив ***ым***  |
| animate accusative   | красив ***ого*** | красив ***ую*** | красив ***ое***  | красив ***ых***  |
| inanimate accusative | красив ***ый***  | красив ***ую*** | красив ***ое***  | красив ***ые***  |
| instrumental         | красив ***ым***  | красив ***ой*** | красив ***ым***  | красив ***ыми*** |
| prepositional        | красив ***ом***  | красив ***ой*** | красив ***ом***  | красив ***ых***  |

There are more things to consider in Russian, but the charts above should be enough to show how nominal declension works.

## Implementation

In this project, I included three masculine, three feminine, and two neuter nouns, as well as three adjectives. It does not sound like much, but it can generate many combination based on the rules.You can use the `russian` predicate to see the output. The syntax is `russian(Word, [Category,Gender,Number,Case,Animate], Meaning)`. You can type `russian(Word, [nounphrase,Gender,Number,Case,Animate], Meaning)` and see all the valid combination (for example, красив ***ая*** девочк ***а*** is valid, and красив ***ый*** девочк ***а*** is not).

## Tradeoff

Russian can be difficult to model, since there are more rules and many exceptions. In this project, I used the most common declension rules and ignore the special cases in Russian so it will be easier for us to see the pattern. Also, I romanize the Russian language to make things easier. Specifically, I use scientific transliteration (more details at [Romanization of Russian](https://www.wikipedia.com/en/Romanization_of_Russian)).
