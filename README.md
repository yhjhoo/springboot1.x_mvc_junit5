# springboot1.x_mvc_junit5

Springboot 1.5.7
Junit 5


POM
```
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.0.0</version>
</dependency>

<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.0.0</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>org.junit.platform</groupId>
    <artifactId>junit-platform-runner</artifactId>
    <version>1.0.0</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>com.github.sbrannen</groupId>
    <artifactId>spring-test-junit5</artifactId>
    <version>1.0.0</version>
    <scope>test</scope>
</dependency>
```


Java
```
@RunWith(JUnitPlatform.class)
@ExtendWith(SpringExtension.class)
@WebMvcTest(WelcomeController.class)
public class SpringbootMvcJunit5ApplicationTests1 {

    @Autowired
    private MockMvc mockMvc;

    @Test
    void contextLoads() throws Exception {
        mockMvc.perform(get("/test")).andExpect(status().isOk());
    }
}
```
