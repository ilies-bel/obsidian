# Cheatsheet Hibernate
## Annotations
 - `@Entity`
 Will map an entity to the table in the DB. 
 Write `@Entity("name") to set the name of this entity.
 By default, the name of the entity is the name of the annotated class
 - `@Id`
 Maps the identifier.
 The annotated attribute will be mapped to the table's primary key.
 
 - `@Table`
 Set the table name. `@Column(name = "Customer")` will be map to the table named "*customer*".
 - `@Column`
 Specifies that the annotated property has to be persisted on a table's column.
 Use `@Column("name")` to set the column name. The property name will be used otherwise.
 - `@GeneratedValue(...)`
 Configures the way the `@Id` attribute should be incremented
   > eg:
   > ```
   > @GeneratedValue(strategy = GenerationType.SEQUENCE, generator="customer_id_seq")
   > ```
   > Uses a sequence named `customer_id_seq` to generate the new ids.
 - `@Embeddable`
 Declares that a class if meant to be embedded within other entities
 - `@Embedded`
 Annotated on top of an attribute, tells the type of the attribute should be embedded (ie: is annotated with `@Embeddable`).
 Use of `@AttributeOverrides ` to customize/override the fields of embeddable types.
 
 - `@Enumerated(EnumType.STRING)`
   Maps enum values to the entity properties:
      - `EnumType.STRING` Store the enum values according to the name of enum value
      - `EnumType.ORDINAL` Store the enum values  according the ordinal position   
   The default value is `EnumType.ORDINAL`
 - `@OneToMany(mappedBy = "...")`
 Maps a Foreign key column, to be part of a **1.p relationship** (One to many)
 
 - `@ManyToOne`
 Maps a Foreign key column, to be part of a **p.1 relationship** (Many to one)
 - `@OnetoOne`
 Maps a Foreign key column, to be part of a **1.1 relationship** (One to one)
 - `@ManytoMany`
 Maps a Foreign key column, to be part of a **p.p relationship** (Many to many)
 - `@Inheritance(strategy=InheritanceType.)`
 Specifies the inheritance strategy.
 `InheritanceType.SINGLE_TABLE` The entities from different classes with a common ancestor are placed in a single table 
 `InheritanceType.JOINED` Each class has its table and querying a subclass entity requires joining the tables
 - `@NotNull `
 The annotated element must not be null.
 - `@NotBlank `
 The annotated String element must not be null and the length is greater than zero.
 - `@Min `
 Min restriction on the numeric annotated entity
 - `@Max `
 Max restriction on the numeric annotated entity
 - `@Email `
 Validate an e-mail address following the standard Email constraint.
 - `@Positive `
 Positive restriction on the annotated entity (0 is considered as an invalid value)
 - `@Negative `
 Negative restriction on the annotated entity
