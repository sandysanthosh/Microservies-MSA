
#### Item.java:

```
@Entity

public class Item{
@Id
@GenereatedValue(strategy = GenerateType.AUTO)

Private Long id;
Private String name
Private Long description;

}
```

#### Item Repo:

```

public interface ItemRepository extends CrudReository<Item,Long> 
{

}

```
#### applicaiton.properties:

```
logging.level.org.springframework:DEBUG

# H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2
spring.datasource.url= jdbc:h2:mem:items

```

#### To Test:

  localhost:8080/items
