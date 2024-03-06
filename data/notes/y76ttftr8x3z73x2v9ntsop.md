
Pour rendre la rapport de test plus lisible déjà améliorer par une convention de nommage inspiré du clean code [[programation.java.tu.convention-de-nommage]]

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

Source:
- https://www.baeldung.com/junit-custom-display-name-generator
