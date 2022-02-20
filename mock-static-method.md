Add Dependency:

<!-- https://mvnrepository.com/artifact/org.mockito/mockito-inline -->
<dependency>
    <groupId>org.mockito</groupId>
    <artifactId>mockito-inline</artifactId>
    <version>4.3.1</version>
    <scope>test</scope>
</dependency>

Code Block:

try (MockedStatic<Utils> utilities = Mockito.mockStatic(Utils.class)) {
            utilities.when(() -> Utils.validateRequest(payload))
                    .thenReturn(violations);
}
