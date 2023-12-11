# ¿Cómo formular una Hipótesis?
1. Se debe Identificar un problema (Parsimonia)
2. Extracción de características (Variables)
3. Preciar conceptos (Ambigüedades)
4. Tipo de Escala de medición (descripción, relaciones y diferencias, medidas de desempeño)
5. Se debe evitar usar variables categóricas (si/no)
# Propiedades de una Hipótesis
    * Debe ser simple, específica e informativa, medible, falsable, verificable, reproducible y conceptualmente clara
      * La Ambigüedad hace que verificación sea muy difícil de confirmar o refutar
      * Existen métodos y técnicas de adquisición de datos y de análisis interactivo de estos.
    * Se deben relacionar al **cuerpo del conocimiento** ya existente, **cinturón protector** (**hipótesis auxiliar informativa**)
    * Su validación aporta conocimiento al área
    * La hipótesis debe ser "**operacionalizable**"
    * La hipótesis se de expresar en términos de variables que puede ser medidas.
## Tipos de variables
### Variables Independientes
      * Son variables que controla el investigador o quién diseña el experimento
      * Son las que el diseñador cambia para estudiar ciertos efectos principales e interacciones que afectan la respuesta.
### Variables Dependientes
      * Son las variables de respuesta que se miden o observan a partir de los cambios deliberados en las variables independientes.
      * Las variables de respuesta dan cuenta de los efectos que producen los cambios en las variables independientes.
  * Test de Hipótesis
    * Teoría de Neyman & Pearson
      * Desarrollaron una teoría para contrastar hipótesis alternativas
      * Consiste en juzgar si cierta hipótesis es compatible con los resultados experimentales y/o datos observados
      * Tipos de Hipótesis
        * Hipótesis Alternativas
          * Hipótesis A v/s Hipótesis B
          * Donde A y B son mutuamente excluyentes (no pueden cumplirse simultáneamente)
          * Hipótesis Nula: ($H_0$) v/s Hipótesis Alternativa: ($H_1$)
        * Hipótesis Anidadas
          * Hipótesis A y B, donde A es un caso especial de B. $A \subset B$
        * Hipótesis Secuenciales
        * Hipótesis Simple sobre $\theta$
          * El parámetro $\theta$ toma un valor único
        * Hipótesis compuesta sobre $\theta$
          * El parámetro $\theta$ se le asignan varios valores.
        * Hipótesis Nula ($H_0$) es la hipótesis que se somete a prueba.
          * Esta hipótesis se mantendrá a no ser que los datos indiquen lo contrario (R)
          * Esta hipótesis nunca se considera probada
        * Hipótesis Alternativa $(H_1)$ ^lbrWeg-GG es la hipótesis del cambio contrapuesta a $H_0$
        * ![[Roam/Turing/Attachments/imgs/app/Turing/22ciiCez7k.png]]
    * ### Elementos de una prueba de Hipótesis
    * Prueba de Hipótesis Estadística
      * Es una regla $\gamma$ (procedimiento) para decidir si rechazamos una hipótesis $H_0$, a partir de los datos obtenidos (experimental u observacional).
    * 1. Hipótesis Nula $(H_0)$ ^WLB7FCy9Y
      * Hipótesis Alternativa $(H_1)$
    * 2. Construir una estadística de Prueba T basada en al m. a. $x_1$, $x_2$, ...,$x_{n-1}$, $x_n$, que no depende de $\theta$
      * Estadística de Prueba
        * Es una función de los datos (Estadística de prueba). Interesa que contenga el máximo de información sobre la hipótesis $H_0$. Es en base a la información contenida en esta estadística que decidiremos respecto de $H_0$
    * Medida de Discrepancia $T(x_1, ..., x_n)$
    * 3. Particionar el espacio de información $X = C \cup C^c$
    * Región de Rechazo $C$
    * Región de Aceptación $C^c$
    * Región Crítica:
      * Define los valores de la estadística de Prueba para los cuales se tiene evidencia contra $H_0$. (No existe una única RC)
    * 4. Regla de Decisión (Se refuta o se mantiene)
      * Regla de Decisión
        * Procedimiento que acepta o rechada $H_0$, dependiendo del valor de la estadística de Prueba: $T(x_1,x_2,...,x:n)$
    * Nivel de significancia
      * Este valor $\alpha$ determina el valor crítico $c$
        * $P(T>c|H_0) = \alpha$
        * El procedimiento de selección de "$c$" a partir de $\alpha$ tiene varias críticas
      * Limitaciones de $\alpha$
        * El resultado del contraste depende de la selección de $\alpha$
        * Este valor sólo nos proporciona el resultado del Contraste (Confirmación/Refutar: Dicotómia V/F)
        * No permite diferenciar entre diversos grados de evidencia que la muestra indica a favor o en contra de $H_0$
        * Valor $p$ (p-value) crítico ó crítico de Fisher.
        * Test severos de Debora Mayo
    * ### Errores y potencia de un Test
      * **Error Tipo I**
        * Rechaza $H_0$ (cuando es verdadero)
        * $P($Error Tipo I$)|H_0) = P_{\theta}(C) = \alpha(\theta)$, $\theta \in \Theta_0$
      * **Error Tipo II**
        * Acepta $H_0$ (cuando es falso)
        * $P($Error Tipo II$)|H_1) = P_{\theta}(C^c) = \beta(\theta)$, $\theta \in \Theta_1$
      * **Función Potencia**
        * Fijada la región crítica $C$ podemos definir la función:
        * $$\pi_C: \Theta \rightarrow [0,1]$$, $$\pi_C(\theta) = P_{\theta}(C)$$ con $$\theta \in \Theta$$
    * ### Distribuciones muestrales
    * ### Tipos de Errores involucrados
      * Neyman-Pearson
        * $$H_0: \theta=\theta_0$$; $$H_1: \theta=\theta_1$$
      * La probabilidad de rechazar erróneamente la hipótesis nula
        * Dado $$\alpha = P(x \in W| \theta_0)$$, con $$W \in \Omega$$
      * Queremos encontrar una región crítica $$W \in \Omega$$ en que minimice la probabilidad de aceptar erróneamente $$H_1$$ (dado que $$H_0$$ es verdadero).
      * $$\beta = P(x \notin W | \theta_1)$$
    * ### Test de Medias (Varianza conocida $$\Sigma^2$$)
      * Caso I
        * $$H_0: \mu = \mu_0$$ v/s $$H_{1}: \mu \neq \mu_0$$
        * Hipótesis Bilateral (dos colas)
          * Rechazar $$H_0 | \mu_0 \leftrightarrow \mid (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma} \mid > Z_{\frac{\alpha}{2}}$$
          * Aceptar $$H_0|\mu_0 \leftrightarrow \mid (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma}\mid \leq Z_{\frac{\alpha}{2}}$$
          * ![[Roam/Turing/Attachments/imgs/app/Turing/pLqCEBx72e.png]]
      * Caso II
        * $$H_0: \mu = \mu_0$$ v/s $$H_{1}: \mu > \mu_0$$
        * Hipótesis Unilateral (cola hacia la derecha)
        * Rechazar $$H_0 | \mu_0 \leftrightarrow \mid (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma} \mid > Z_{\alpha}$$
        * Aceptar $$H_0 | \mu_0 \leftrightarrow (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma} \leq Z_{\alpha}$$
        * ![[Roam/Turing/Attachments/imgs/app/Turing/Mwi0mLe6zA.png]]
      * Caso III
      * $$H_0: \mu = \mu_0$$ v/s $$H_{1}: \mu < \mu_0$$
      * Hipótesis Unilateral (cola hacia la izquierda)
      * Rechazar $$H_0 | \mu_0 \leftrightarrow (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma} < Z_{\alpha}$$
      * Aceptar $$H_0 | \mu_0 \leftrightarrow (\overline{X}-\mu_0)\frac{\sqrt{n}}{\sigma} \geq Z_{\alpha}$$
      * ![[Roam/Turing/Attachments/imgs/app/Turing/zeV2j6gTxJ.png]]
    * ### Calculo de Error Tipo II
      * $$H_0: \mu = \mu_0$$ v/s $$H_1: \mu \neq \mu_0$$
      * Con Hipótesis Bilateral
      * $$\beta(\mu) = P_{\mu}(Aceptar H_0 | H_1) = P_{\mu}(\mid \frac{\overline{X}-\mu_0}{s/\sqrt{n}} \mid \leq Z_{(\alpha/2;n-1)})$$
      * Región iguales colas
      * $$\beta(\mu) = P_{\mu}(\mid \frac{\overline{X}-\mu_{0}}{s/\sqrt{n}} \mid \leq Z_{(\alpha/2;n-1)}) = P_{\mu}(-Z_{\alpha/2} \leq \frac{\overline{X}-\mu_0}{s/\sqrt{n}} \leq Z_{\alpha/2}) = \Phi(\frac{\mu_{0}-\mu}{s/\sqrt{n}}+ Z_{(\alpha/2;n-1)} - \Phi(\frac{\mu_{0}-\mu}{s/\sqrt{n}} - Z_{(\alpha/2;n-1)})$$
      * Error tipo II; depende de $$\mu$$
    * ### Potencia de la Prueba
      * $$\Pi(\mu)= 1 - \beta(\mu)$$
    * ### Valor critico p de Fisher
      * {{table}}
        * $$H_0$$
          * $$H_1$$
            * Valor $$p$$
        * $$\mu = \mu_0$$
          * $$\mu \neq \mu_0$$
            * $$2P_\mu(Z \geq Z_0)$$
        * $$\mu \leq \mu_0$$
          * $$\mu > \mu_0$$
            * $$P_\mu(Z \geq Z_0)$$
        * $$\mu \geq \mu_0$$
          * $$\mu < \mu_0$$
            * $$P_\mu(Z \leq Z_0)$$
      * Valor Critico $$p = P(Z \geq Z_0)$$
      * Valor Critico $$p=P(Q \geq Q_0)$$
    * ### Tamaño muestral
      * $$\beta(u) = $$ error tipo II
      * $$\beta = \beta(\mu_1)$$, $$\mu_1$$ fijo
      * $$n = \frac{(Z_{\alpha/2} + Z_{\beta})^2 \sigma^2}{(\mu_1 - \mu_0)^2}$$
    * ### Estadísticas para descubrimiento
    * El resultado fundamental de Neyman & Pearson nos dice
      * Test definido
        * $$\varphi(x) = \frac{p(x|\theta_0)}{p(x|\theta_1)} > k_{\alpha}$$
        * Es el test que minimiza el error de Tipo II dado un error de Tipo I definido (test uniformemente máximo PUM)
        * Notar que sólo existe un test PUM para hipṕotesis "simples" donde ambas distribuciones se encuentran completamente especificadas
          * $$H_0: \theta=\theta_0; H_1: \theta=\theta_1$$
        * $$H_0: \theta \in \theta_0; H_1: \theta \in \theta_1$$
    * El resultado fundamental de Neyman & Pearson nos dice
      * Test definido como
        * $$\varphi = \frac{p(x|\theta \in \theta_0)}{p(x|\theta \in \theta_1)}$$
        * El error de Tipo II depende de $$\theta \in \Theta_0$$  y el error de Tipo I depende de $$\theta \in \Theta_0$$ definido (test uniformemente máximo PUM no existe)
        * Notar que no existe un test PUM para hipótesis "compuestas" donde ambas distribuciones se encuentran completamente libres.
    * ### Estadística medida de discrepancia
      * En un conjunto de datos podemos definir el test de **razón de verosimilitud** como
        * $$\Lambda(x)= \frac{L(\theta_0 | x)}{L(\theta_1|x)}$$
      * Para hipótesis simples, donde $$L(x|\theta)$$ es la función de verosimilitud
        * $$L(\theta|x_1;x_2;...;x_n) = p(x_1;x_2;...;x_n| \theta \in \Theta_0)$$
      * Para hipótesis compuestas debemos acudir a la versión del test de **razón de verosimilitud generalizado**
        * $$\Lambda(x)= \frac{Sup_{\theta \in \Theta_0} L(\theta | x)}{Sup_{\theta \in \Theta_1} L(\theta|x)}$$
      * Wilks (1938), bajo ciertas condiciones de regularidad se cumple que
        * $$-2\ln \Lambda(x) \approx \chi^2_p$$
        * Esto nos permite definir niveles de confianza para nuestro test (vaolres $$p$$)
        * El valor $$p$$ se define como la probabilidad, asumiendo la hipótesis nula, de encontrar datos de igual o mayor incompatibilidad a la predicción de la hipótesis
          * En física se suele convertir en un estadístico equivalente definido como **Z**, el número de desviaciones estándar que una variables aleatoria normal estándar sea encontrada con probabilidad $$1-p$$ sobre su valor esperado
            * $$Z=\Phi^{-1}(1-p)$$
          * De esto se deriva el famoso valor $$5\sigma$$, valor estándar para afirmar un descubrimiento (usado en bosón de Higgs)
            * $$p=2.87 \times 10^{-7}$$
    * ### Enfoque Bayesiano
      * La escuela Bayesiana sostiene que hay un error radical en las corrientes epistémicas anteriores.
      * El enfoque Bayesiano Fundamente su postura en
        * Teoría de probabilidades (Regla de Bayes)
        * Inapropiada asignación de probabilidad a una teoría (cero) bien confirmada)
        * Se expresa con probabilidades condicionadas
        * **Inferencia Causal**
      * Uno de los problemas de la Ciencia es como asignar probabilidades a las teorías / hipótesis plausibles.
        * "h" en base a una evidencia "e"
      * El enfoque Bayesiano fundamenta su postura en el conocimiento de 
        * $$P(e|h)$$
        * Recurre a la Teoría de probabilidades (Regla de Bayes)
      * Sea $$P(h)$$ la probabilidad asignada a priori a la hipótesis "h" (creencia) en ausencia de todo conocimiento de la evidencia "e"
      * Sea $$P(e)$$ la probabilidad asignada a la evidencia "e" en ausencia de cualquier supuesto respecto a la teoría "h"
      * $$P(h|e)=P(h)\frac{P(e|h)}{P(e)}$$
        * Probabilidad asignada a posteriori a "h" dada la prueba o evidencia "e"
      * **Ejemplo**
        * La $$P(h)$$ probabilidad previa asignada a "h" se modifica por un factor de escala $$[\frac{P(e|h)}{P(e)}]$$ en función de prueba "e"
        * $$P(e|h)$$ es máxima, es decir 1, si "e" se sigue de "h"
        * $$P(e|h)$$ es minima, es decir 0, si la negación de "e" se sigue de "h"
        * $$P(h|e)=P(h)\frac{P(e|h)}{P(e)}$$
        * $$[\frac{P(e|h)}{P(e)}]$$ se considera como un factor de escala
          * Donde su divisor $$P(e)$$ es desconocido
          * $$P(e) = P(e|h) P(h) + P(e|\underline{h}) P(\underline{h})$$
            * Donde $$P(\underline{h})$$ se refiere a todas las hipótesis no "h"
            * El número de hipótesis plausible $$\underline{h}$$ puede ser finito o infinito
          * $$P(e)$$ es la medida de certeza de la prueba o evidencia "e"
            * Es altamente probable tanto si  supone la hipótesis "h", como si no la supone
          * La hipótesis "h" puede no recibir un apoyo importante de "e"
          * La evidencia "e" es improbable a menos que suponga la hipótesis "h"
          * La hipótesis "h" recibe una alta confirmación si se confirma la prueba o evidencia "e"
          * Interpretar
            * $$P(e|h) \approx 1$$
            * $$P(e|h) \approx 0$$
      * ### Enfoque Bayesiano Objetivo (BO)
        * Asigna de manera racional las probabilidades a la verosimilitud de ganar y con estas probabilidades previamente asigandas se pueden modificar las hipótesis usando nueva evidencia.
          * Carreras de caballos asigna a los caballos una probabilidad condicionada por el conocimiento que tiene el jugador sobre el comportamiento de los caballos en el pasado. Además dichas probabilidades están sujetas a cambio a la luz de nuevas pruebas o evidencias.
      * ### Enfoque Bayesiano Subjetivo (BS)
        * Las probabilidades que maneja el teorema de Bayes representan distintos grados de creencia de los investigadores.
        * Comprender el conocimiento científicos en términos de creencias es un punto de partida decepcionante
        * El BS asigna consistentemente las probabiliades según el grado de creencia evitando así las dificultades de los BO
        * El grado de crencia del BS es clave para comprender la Ciencia y su Historia.
        * El problema importante consiste en estimar el grado de creencia
          * Enfoque Bayesiano v/s Lógica deductiva
        * Ejemplo
          * Dos investigadores comienzan estando fuertemente en desacuerdo acerca de la probable verdad de la hipótesis "h", que predice un outliers.
          * El que le asigna una probabilidad alta a "h" pensará que "e" es menos improbable que aquel que asigna una probabilidad baja a "h"
          * El $$C_1$$ atribuye una alta probabilidad "h"
          * Sea
            * $$P(h|e) = P(h)[\frac{P(e|h)}{P(e)}] = \frac{P(h)}{P(e)}$$ escala a valores más altos
            * Puesto que "e" sigue de "h" $$P(e|h) = 1$$
          * El $$C_2$$ atribuye una baja probabilidad "h"
            * La escalará a un valor mayor que el $$C_1$$$$
            * Según llegan más pruebas positivas él que dudaba al comienzo se verá obligado a escalar la probabilidad  aproximándose al científico convencido inicialmente.

  * ## Proyecto
    * ### Elementos del Proyecto
      * 1. Definición del tema
      * 2. Revisión del estado del arte
      * 3. Propuesta de solución basada en problemas similares
      * 4. Desarrollo analítico de la solución propuesta
      * 5. Diseño del algoritmo o de la solución
      * 6. Implementación
      * 7. Prueba y depuración
      * 8. Estudio experimental
      * 9. Documentación
    * ### Metodología y plan de trabajo
      * 1. Aportes y resultados esperados
      * 2. Formas de validación
      * 3. Recursos disponibles
      * 4. Recursos solicitados
      * 5. Referencias bibliográficas