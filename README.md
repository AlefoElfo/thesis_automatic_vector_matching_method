# Diálogo sema onomasiológico. Teoría, método y resultados para el *Diccionario de la Reforma Protestante*
*Tesis*

## Explicación

Aquí se muestran los resultados finales de la tesis, la cual estará disponible una vez sea presentada, aprobada y publicada.

Se almacenan en un jupyter notebook. Para mayor comodidad se recomienda abrirlo desde :link: [Google Colab](https://colab.research.google.com/github/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb) o, si se prefiere, desde aquí mismo, en :link:[GitHub](https://github.com/AlefoElfo/nlp.onomasiology.thesis/blob/main/Tesis_PLN_y_di%C3%A1logo_sema_onomasiol%C3%B3gico.ipynb). 

Las principales secciones son:
- Diccionario de la Reforma Protestante
- Pregunta natural al diccionario
- Respuesta para el usuario
- Evaluaciones
- Conclusiones

Hasta abajo hay una sección con todas las funciones ('Funciones. Compendio'), para facilitar la exploración.

## Conclusiones
### Primera evaluación del modelo
Pregunta|Lexema esperado|¿Acertó?
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

**Columnas**
- "Pregunta": La pregunta hecha por un usuario ficticio al diccionario
- "Lexema esperado": El término esperado[^1]
- "¿Acertó?": Si salió el lexema esperado en una lista de 30 posibles resultados
  - 10 principales similitudes con la lista de lexemas
  - 10 principales búsquedas con las definiciones
  - 10 principales búsquedas con la información extra


### Segunda evaluación del modelo
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

**Columnas**
- "Test":  Lista de test que se hicieron al modelo
- "Pregunta": La pregunta hecha por un usuario ficticio al diccionario
- "Lexema esperado": El término esperado[^2]
- "¿Acertó":  Si salió el lexema esperado en una lista de 20 posibles resultados
  - 10 principales búsquedas con las definiciones
  - 10 principales búsquedas con la información extra
- "¿Acertó lexema?":  Si salió el lexema esperado en una lista de 10 posibles resultados. Estos resultados fueron comparados exclusivamente con los términos

[^1]: Aunque en la tesis se utiliza "término", en este trabajo se utilizó "lexema" para evitar la confusión semántica entre "término" y la flexión verbal "termino", al momento de programar
[^2]: *Ídem*
