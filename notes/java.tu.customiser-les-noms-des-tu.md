---
id: y76ttftr8x3z73x2v9ntsop
title: Customiser Les Noms Des Tu
desc: ''
updated: 1708520437476
created: 1708520437476
isDir: false
---
2023-02-12

Pour rendre la rapport de test plus lisible déjà améliorer par une convention de nommage inspiré du clean code [[java.tu.convention-de-nommage]]

Possible de customiser en remplacement les underscore par des espaces : 
```
@DisplayNameGeneration(DisplayNameGenerator.ReplaceUnderscores.class)
class ReplaceUnderscoresGeneratorUnitTest {

    @Nested
    class when_doing_something {

        @Test
        void then_something_should_happen() {
        }

        @Test
        @DisplayName("@DisplayName takes precedence over generation")
        void override_generator() {
        }
    }
}
```


--- 
Tags: #programmation #java #TU 

Source:
- https://www.baeldung.com/junit-custom-display-name-generator
