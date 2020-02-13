# SQL
  É unha linguaxe declarativa que nos permite acceder e manipular unha base de datos.
  A consulta mínima está formada polo SELECT e o FROM.
  
#### SELECT
   Conforma os elementos da tabla que se vai a mostrar. Filtra e selecciona columnas.
   Cando no SELECT hay un reductor (COUNT ou calquera reductor(sum, avg, max)) no GROUP BY poranse os atributos anteriores ao reductor.    Por exemplo:
    _Do SELECT goal.matchid, game.mdate, COUNT(*), no GROUP BY porase (goal.matchid, game.mdate)_

#### FROM
   No FROM escribese a taboa de onde se van a coller os datos.
  
#### WHERE
  Función básica para as consulta. Filtra e selecciona filas/tubla. Vai despois do SELECT e do FROM. Nel situase o denominado predicado (función que devolve un true ou un false). Para filtrar compara dous ou máis elementos: o que se quere comparar e ao que se quere comparar. Neste predicado pódense aplicar métodos como:
  
  * LIKE: esta función sirve para comparar cadenas (palabras). Aplicando o signo %.  O que vai dentro do LIKE é unha expresión regular.             Vai entre comillas simples.  “S%”, por exemplo buscaría todos os datos  que empezaran por S e o seguiran 0 ou varios elementos.           Si se pon un ”_”  é para substituir o número de posición polo numero de barras baixas. Por exemplo “_S%” vai a buscar todo o que           teña como segunda posición unha S.
  * =: Cando usamos un “=”  e  o do outro lado é unha cadena.  “ S%”, por exemplo buscaría un dato que se chamara S% tal cual.
  * IN: Chequea que o que se solicita está na lista. Todo o que vaia entre paréntesis non ten nada que ver co resto, é independente.
  * BETWEEN: incluye os límites e leva un AND.
  * <> : distinto de

#### GROUP BY
  Vai a facer  una subtaboa cos elementos (sin repetir) de SELECT.
  
#### ORDER BY 
  Sirve para ordenar os elementos da taboa según un criterio. Si queremos que sea en orden ascendente, escribese ASC e en orden descendente, DESC.
  
#### HAVING
  Aplícase a cada unha das subtaboas creadas polo GROUP BY e leva un predicado.
  
#### JOIN
  É un producto cartesiano. permite mesturar taboas para coller datos de dúas ou máis taboas á vez. Cando no Join van dous atributos iguais (actor JOIN actor), hay que diferencialos mediante AS (actor AS Actor JOIN actor AS Actor2).
	
  ON: Restringe o resultado. A continuación del, ponse o predicado. Na maior parte dos casos o predicado é a relación clave principal-clave foránea. O ON pode sustituirse poñendoo no predicado do WHERE. O orden dos elementos do predicado non influe no resultado.
  
  O LEFT JOIN saca todos os da esquerda  aínda que os da dereita sexan nulos. O RIGHT JOIN saca todos os a da dereita aínda que os da esquerda sexan nulos. Si solo se pode empregar un ou outro, cambiaranse de orden os atributos según o que se pida.

  Para seleccionar elementos dunha taboa en concreto usase o nome da taboa, punto, e o que se quere mostrar. Introdúcese despois co SELECT.

#### NULL
   Pode levar un NOT (opcional). Non pode existir un “=” cando se emplea un NULL. Tampouco se poden usar expresions regulares cando se usa un NULL.

#### Reductores
  * SUM: Suma os valores que se lle pasen. Vai entre paréntesis  os elementos.      Considerase reductor.
  * AVG: fai a media dos elementos que se soliciten. 
  * MAX: colle o valor máximo dos que se lle pasan. 
  * MIN: colle o valor mínimo dos que se lle pasan.

#### Outras funcions
  * __DISTINCT__ 
  Despois do SELECT, selecciona elementos sen repetidos.
  * __COUNT__ 
  Conta o número de elementos que se desexe. Pode funcionar co ou sin GROUP BY. Os elementos van entre paréntesis. Por exemplo, COUNT (dept.name). Se non hai GROUP BY, habrá só unha subtaboa, que é a propia táboa, dependendo da cantidade de elementos do FROM.
  * __REPLACE__ 
  Sirve para sustituir todas as instancias de un valor dunha cadena especificando o outro valor da cadena. A estrutura é (‘cadena de onde se quere sustituir’, ‘o que se quere sustituir’, ‘polo que se quere sustituir’)
  * __ROUND__
  Redondea o valor que se lle pasa (normalmente unha conta) e indicándolle o número de unidades de redondeo. Se o número indicado é positivo, redondea a tantos números decimais como o número indicado. Por exemplo, (_population*gdp_, 3) redondea o número con tres decimais), se o número é negativo aproxima a decenas, centenas ou incluso a miles, depende do número indicado. Por exemplo (_population*gdp_, -3) aproxima a miles.
  * __AS__  
  Sirve para renombrar o nome das columnas do resultado. Sitúase no SELECT. Cando se quere escribir máis de unha palabra, ponse a cadena entre comillas simples.
  * __COALESCE__ 
  Sustitúe o valor NULL por outro valor desexado. Sitúase no SELECT e a súa estrutura é (o atributo con NULLS, polo que se quere escribir ‘’). Por exemplo (dept.name, ‘None’)
  * __CASE__ 
  Péchase co END. Sitúase no SELECT. E depois del escríbese WHEN, o cal impón a condición. No caso contrario situase o ELSE. A estructura é a seguinte, como se mostra no seguinte exemplo (teacher.dept IN (1,2) THEN ‘Sci’ ‘Art’).
  * __CONCAT__
  Sirve para devolver unha cadena resultante da concatenación de dous ou máis valores. Normalmente no SELLECT.
  
#### OLLO, TODA CONSULTA SQL DEBE REMATAR EN ;



  
