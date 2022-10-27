# Resultados con método automático por similitud de vectores
> Tesis: Diálogo sema onomasiológico. Teoría, método y resultados para el *Diccionario de la Reforma Protestante*

## Explicación

Aquí se muestran los resultados finales de la tesis, la cual estará disponible una vez sea presentada, aprobada y publicada.

Se almacenan en un *jupyter notebook*. Para mayor comodidad se recomienda abrirlo desde :link: [Google Colab](https://colab.research.google.com/github/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb) o, si se prefiere, desde aquí mismo, en :link:[GitHub](https://github.com/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb). 

Las principales secciones son:
- Diccionario de la Reforma Protestante
- Pregunta natural al diccionario
- Respuesta para el usuario
- Evaluaciones
- Conclusión


Hasta abajo del :link: [notebook](https://colab.research.google.com/github/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb) hay una sección con todas las funciones para facilitar la exploración ('Funciones. Compendio'). Es **importante** aclarar que el diccionario sólo tiene 70 términos y no todos tienen mucha información. A mayor información crecerá la fidelidad, pues el modelo tendrá más datos por analizar.

El código es totalmente libre, pero no el contenido del diccionario: sus términos, definiciones e información extra. El diccionario está registrado para proteger los derechos de autor. **No plagies mi trabajo, mejor apóyame para terminarlo.** *Mejores son dos que uno; porque tienen mejor paga de su trabajo (Ecl 4.9)*. [Diccionario de la Reforma Protestante](https://www.facebook.com/DiccionarioReforma)
## Primera evaluación del modelo
Se omiten las "Preguntas con contenido ajeno al diccionario" y "Preguntas con contenido relacionado, pero sin lexema al que se alude", las cuáles sí están disponibles en el :link: [notebook](https://colab.research.google.com/github/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb).

### Resultados
**Pregunta**|**Lexema esperado**|**¿Acertó**?
|:---|:---|:---|
Documento que quemó Martín Lutero|Exsurge Domine|Sí
Tipo de monje que era martín Lutero|Orden de San Agustín|No
Batallas entre católicos y protestantes|"Guerra de los ochenta años". No mostró "Guerra de Esmalcalda"|Parcial
Dónde se enfrentó Lutero a Carlos quinto|Dieta de Worms|Sí
Escrito de martín lutero a los principales alemanes|A la nobleza cristiana de la nación alemana|Sí
Precursores de la reforma|"Husita", "Remonstrante", "Gomarista". Faltó "Valdense"|Parcial
Documento donde se excomulga a Lutero|Decet Romanum Pontificem|Sí
Escrito más famoso de Martín Lutero|Noventa y cinco tesis|Sí
Cómo se llama cuando el pan y el vino se hacen el cuerpo de Cristo|Eucaristía. Transubstanciación|Sí

### Columnas
- "Pregunta": La pregunta hecha por un usuario ficticio al diccionario
- "Lexema esperado": El término esperado[^1]
- "¿Acertó?": Si salió el lexema esperado en un total de 30 posibles similitudes
  - 10 principales similitudes con la lista de lexemas
  - 10 principales similitudes con la información extra
  - 10 principales similitudes con las definiciones


## Segunda evaluación del modelo
### Resultados
Test|Pregunta|Lexema esperado|¿Acertó?|¿Lexema acertó?
:---|:---|:---|:---|:---
t1|pastor de la iglesia valdense|Barba.|No|No|
t2|himno de la reforma protestante|Castillo fuerte es nuestro Dios.|Sí|-|
t3|documento que lutero escribió para los curas y sacerdotes católicos|Cautividad babilónica de la Iglesia, La|Sí|-|
t4|Principales postulados de la Reforma protestante|Cinco Solas.|No|No|
t5|cómo se llama cuando el pecado afecta totalmente al hombre|Cinco puntos calvinistas. 1. Totalidad depravada.|Sí|-|
t6|Quiénes son los que solo creen en la Biblia y nada más|Cinco solas. Sola Scriptura.|Sí|-|
t7|cómo se llama el concilio donde hablaron de Lutero|Concilio. Concilio de Trento.|No|No|
t8|cuándo excomulgaron a Lutero|Decet romanum pontificem.|Sí|-|
t9|que sólo recordamos a Cristo y no que él está presente|Eucaristía. Anamnesis.|No|No|
t10|qué le escribió Martín Lutero al papa?|De la libertad del cristiano.|Sí|-|
t11|cómo se dice cuando Jesús se convierte en pan y vino|Eucaristía. Transubstanciación.|Sí|-|
t12|calvinistas de los países bajos|Gomarista.|Sí|-|
t13|Guerra que perdieron los protestantes|Guerra de Esmalcalda.|Sí||
t14|cómo se llama el grupo de protestantes que muchos fueron asesinados|Hugonote, grupo.|No|Sí|
t15| quiénes son los seguidores de Wyclif|Lolarda, grupo.|No|No|
t16|cómo se llama el tratado que puso fin a la guerra de católicos y protestantes|Paz de Augsburgo.|No|No|
t17|documento en el que los nobles alemanas defienden la reforma protestante en su país|Protesta de Espira|No|No|
t18|cómo se llama la iglesia de los menonitas|Anabaptista, iglesia|No|No|
t19|cuáles son los documentos más importantes de la iglesia católica|Bula.|No|No|
t20|cuál es la enseñanza de Calvino que dice que la salvación no se pierde|Cinco puntos calvinistas. 5. Perseverancia de los Santos.|Sí|-|

### Columnas
- "Test":  test que se hicieron al modelo, del 1 al 20
- "Pregunta": La pregunta hecha por un usuario ficticio al diccionario
- "Lexema esperado": El término esperado[^2]
- "¿Acertó":  Si salió el lexema esperado en una lista de 20 posibles similitudes
  - 10 principales similitudes con las definiciones
  - 10 principales similitudes con la información extra
- "¿Acertó lexema?":  Si salió el lexema esperado en una lista de 10 posibles similitudes. Estos resultados fueron comparados exclusivamente con los términos

## Conclusión
**El proceso onomasiológico sí se logra** con una fidelidad de:
 - 77% (Primera evaluación) 
 - 50% (Segunda evaluación) 

Un 50%, y en un escenario controlado, puede mostrar un modelo poco alentador; pero se ha reducido abismalmente el problema que motivó la tesis:

> <mark>Los diccionarios no pueden ofrecer sus significados expuestos ni precisarlos si los lectores desconocen u olvidan los significantes.</mark>

Ahora, en sentido figurado, no hace falta encontrar una aguja en un pajar, sólo basta tirar una moneda al aire. Pero La tasa de éxito debe mejorar mucho. Esto se puede lograr con:
 - :link: [Pipelines](https://spacy.io/usage/processing-pipelines) personalizadas desde spaCy
 - Una mayor cantidad de términos, definiciones e información extra
 - Un lenguaje más claro al momento de definir
 - Un lenguaje intencional para que haya una mayor tasa de éxito
 - Un nuevo modelo que contemple herramientas mucho más avanzadas, con Inteligencia Artificial[^3]
   - Machine Learning
   - Deep learning
   - Redes neuronales artificiales

### Problemas por resolver
Los pocos términos en el diccionario reducen mucho la capacidad de respuesta del modelo. Se necesita aumentar los términos, las definiciones y la información extra. También agregar biografías.

Uno de los mayores problemas es la diferencia de longitud en la información extra. Por ejemplo, "tipo de monje que era Martín Lutero" no encontró similitudes porque tiene mucha información, a pesar de que contiene las mismas palabras: monje, Martín, Lutero.

Otro problema es cuando la pregunta del usuario tiene alta coincidencia con términos que podrían considerarse secundarios. En la pregunta "Batallas entre católicos y protestantes" hay una similitud con el término "Anabaptista, Iglesia" de un 79.99% contra el 73.64% del lexema esperado, "Guerra de los ocienta años". Esto se debe a que "Anabaptista, iglesia" tiene más palabras y estas crean confusión al modelo: desacuerdo, pena capital, rechazan, controversia, menonitas, huteritas, bautistas, amish.

### Comentarios finales:
 - El modelo ayuda a descubrir sesgos al momento de definir términos
 - Se traza un camino hacia un mejor modelo que eleve el porcentaje de similitud y que disminuya el porcentaje de similitud con palabras secundarias.




[^1]: Aunque en la tesis se utiliza "término", en este trabajo se utilizó "lexema" para evitar la confusión semántica entre "término" y la flexión verbal "termino", al momento de programar
[^2]: *Ídem*
[^3]: Más allá de la capacidad del tesista
