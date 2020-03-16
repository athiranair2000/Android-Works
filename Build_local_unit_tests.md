<h2> Building local unit test files </h2>

Types of dependencies associated with unittests determines which tool you use.

- Android framework:

Particularly complex interactions with the framework, include framework dependencies.

- Minimal android dependencies:

Include mock dependencies using mock framework like Mockito.

<Set up testing environment>

- Store local unit test files at module-name/src/test/java/

- Configure the testing dependencies to use the standard APIs provided by the JUnit 4 framework.

- Specify following dependencies in build.gradle file:

dependencies {
    // Required -- JUnit 4 framework
    testImplementation 'junit:junit:4.12'
    // Optional -- Robolectric environment
    testImplementation 'androidx.test:core:1.0.0'
    // Optional -- Mockito framework
    testImplementation 'org.mockito:mockito-core:1.10.19'
}

<h2>Create a local unit test class </h2>

- Step1: Creating a basic JUnit 4 test class

 -- A test method begins with @Test annotation and contains the code to exercise and verify a single functionality.
 
import com.google.common.truth.Truth.assertThat;
import org.junit.Test;

public class EmailValidatorTest {
    @Test
    public void emailValidator_CorrectEmailSimple_ReturnsTrue() {
        assertThat(EmailValidator.isValidEmail("name@email.com")).isTrue();
    }

