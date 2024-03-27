## SPRING BOOT:
- Offre deux fonctionnalités principales :
   1-auto-configuration   2-starters
- AVANTAGE : un framework qui permet de demarrer rapidement le dev d'un application spring
creer stand-alone Spring application avec integration tomcat
En creant le projet on ajoute les dependances et s'occupe de les gerer
Pas besoin de gerer la configuration si on active l'auto-configuration via l'annotation  @EnableAutoConfiguration

## Annotations :
- @SpringBootApllication est la composante de trois annotations (@Configuration, @EnableAutoConfiguration, @ComponentScan)
- @RestController pour indiquer à spring que la classe du controller
- @RestController avec cette annotation spring utilise la dependence JACKSON pour traduire un object java en json
- @GetMapping(value="Produits/{id})
- @Repository pour le DAO
- @Autowired permet a spring d'instecier automatiquement la dependance injecter
- @PathVariable pour recuper un param depuis l'uri et le passer en param de la methode
- @PostMapping pour les methode d type post
- @RequestBody permet de  chercher dans le body de la requette le json et de le parser pour constituer l'objet en param
- @JsonIgnore sur une propriété pour cacher cette properté dans json
- @JsonIgnorePropeties(value={"pp1","pp2"}) pour cacher des ppte1 et 2

**Deux facon de definir 'l'uri des methode :**
@RequestMapping(value="/Produits", method=RequestMethod.GET) et dans le cas de post : RequestMethod.POST
@GetMapping(value="/Produits")
@GetMapping   indique d'emblée qu'elle répondra aux requêtes de type GET, il n'y a pas besoin de préciser cela que pour  
@RequestMapping  qui peut accepter POST et GET.

**Code http**
- Envoyer le bon code http en utilisant ResponseEntity. ResponseEntity est une classe qui hérite de HttpEntity,  qui permet de définir le code HTTP
à retourner. L'interêt de ResponseEntity est de nous donner la main pour personnaliser le code facilement.

  
## SPRING DATA JPA
SPRING DATA JPA : un framework de la famille spring data : qui permet d'automatiser la creation de la couche d'accès au donnée
Pour utiliser Sprind Data jpa, on ajoute @Repository sur la classe DAO, on transforme l'objet en entite
Spring Data JPA contient un certain nombre de methode pour manipuler les données : findById, save findAll Pour beneficier de ces methodes, on doit
heriter de JpaRepository<Entity, leTypeDeSonId > 