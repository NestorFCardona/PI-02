
<h1 align='center'>
 <b>PROYECTO INDIVIDUAL 
 NESTOR CARDONA</b>
</h1>
 
 <h2 align="center">Cryptocurrency Market Data Analytics</b>
</h2>


Análisis de datos del mercado de criptomonedas, es el último proyecto individual de la etapa de labs. En esta ocasión, se hizo un trabajo con el rol de ***Data Analyst***.
<p align='center'>
<img src = 'https://i0.wp.com/criptotendencia.com/wp-content/uploads/2023/07/Reino-Unido-rechaza-regular-el-trading-minorista-de-criptomonedas.jpg' height = 200>
<p>

## **Descripción del problema: Contexto y Rol a desarrollar**

### **Contexto**

El mercado de criptomonedas es un ecosistema financiero digital en rápido crecimiento donde se crean, negocian y utilizan activos digitales descentralizados, conocidos como criptomonedas. Basadas en tecnología blockchain, estas monedas digitales permiten transacciones seguras y transparentes sin intermediarios. Bitcoin, la primera criptomoneda, inauguró este mercado en 2009, y desde entonces, miles de criptos han surgido, cada una con sus características y aplicaciones únicas. La inversión y el comercio de criptomonedas son populares debido a su potencial de alta rentabilidad, pero también presentan riesgos debido a la volatilidad del mercado. La tecnología subyacente y su impacto en finanzas, tecnología y más áreas siguen siendo temas de exploración en constante evolución.

### **Rol Analista de Datos**

La empresa Tecum Business Ltd., de servicions financieros ha asignado la tarea de realizar un análisis exhaustivo utilizando datos de la API CoinGecko para entender mejor el mercado de criptomonedas y presentar los hallazgos y recomendaciones en un informe detallado.

Se ha solicitado acotar el trabajo en al menos 10 criptomonedas, y en base a estas presentar los análisis y recomendaciones.

 <h1 align="center">REPORTE DEL PROYECTO</b>
</h1>

El criterio de selección de las criptomonedas fue: `LAS 10 CRIPTOMONEDAS MÁS USADAS Y COTIZADAS PARA EL AÑO 2023`, segun la revista especializada CoinDesk, aunque no hay una lista definitiva ya que esto depende de varios factores y puede variar según la fuente. Sin embargo, basándome en los resultados que encontré, estas criptomonedas cumplen con ambos criterios:

## **Las 10 Criptomonedas Seleccionadas**

- **Bitcoin (BTC)**: Es la criptomoneda `más antigua, conocida y valiosa del mercado`. Su precio ha superado los 60.000 dólares en varias ocasiones y se espera que siga creciendo a largo plazo. Su uso es amplio y aceptado en muchos países y plataformas.

- **Ethereum (ETH)**: Es `la segunda criptomoneda más grande y líder en contratos inteligentes`, dApps y tokens no fungibles. Su precio ha alcanzado máximos históricos de más de 4.000 dólares y se espera que aumente con la llegada de Ethereum 2.0.

- **Binance Coin (BNB)**: Es la criptomoneda nativa del exchange Binance, el más grande y popular del mundo. `Su precio ha subido más de un 1.000% en el último año y se espera que siga creciendo por la demanda` y el uso de los servicios de Binance.

- **Cardano (ADA)**: Es una de las criptomonedas `con más potencial de crecimiento, debido a su enfoque científico y académico`. Su precio ha superado los 2 dólares y se espera que aumente con el lanzamiento de contratos inteligentes y otras mejoras.

- **Solana (SOL)**: Es una de las plataformas más rápidas y baratas del mercado, capaz de procesar más de 50.000 transacciones por segundo. `Su precio ha subido más de un 10.000% en el último año y se espera que siga creciendo`por su innovación y adopción.

- **Polkadot (DOT)**: Es una plataforma que busca conectar diferentes blockchains y permitir la transferencia de datos y activos entre ellas. Su precio ha superado los 40 dólares y `se espera que aumente con el desarrollo de su ecosistema` descentralizado e innovador.

- **Uniswap (UNI)**: Es uno de los protocolos `más populares para intercambiar diferentes tokens sin intermediarios, usando un sistema de liquidez descentralizado.` Su precio ha superado los 40 dólares y se espera que aumente con el lanzamiento de nuevas mejoras y funcionalidades.

- **Tether (USDT)**: Es una criptomoneda que `está vinculada al valor del dólar estadounidense, es decir, cada USDT equivale a un dólar.` El USDT es una de las criptomonedas existentes más consistentes del mercado. Su objetivo es facilitar las transacciones entre diferentes criptomonedas y monedas fiduciarias, evitando las fluctuaciones de precios. Es decir, el USDT es una de las criptomonedas existentes más consistentes del mercado.

- **Ripple (XRP)**: Es la moneda de la red Ripple, que `ofrece soluciones de pago rápidas y baratas para instituciones financieras y empresas.`  Su precio ha superado el dólar y se espera que aumente si resuelve sus problemas legales con la SEC.

- **Dogecoin (DOGE)**: Es una criptomoneda basada en un meme, que `tiene un valor basado en la popularidad y el humor`. Su precio ha superado los 0,70 dólares y se espera que aumente si recibe el apoyo de personalidades influyentes como Elon Musk .

## **EDA: Exploratory Data Analysis**

`Inicialmente fue la selección de las 10 criptomonedas: 
Bitcoin (BTC), Ethereum (ETH), Binancecoin (BNB), Cardano (ADA), Solana (SOL), Polkadot (DOT), Uniswap (UNI),Tether (USDT), Ripple (XRP) y Dogecoin (DOGE)` 

Los Análisis de las criptomonedas suelen ser a Corto Plazo (Intradia o diario), Mediano Plazo (Semanal o Mensual) y a Largo Plazo (Trimestral o Anual)

Este proyecto se basó en Analisis a Mediano y principalmente a Largo Plazo, es decir, KPIs anuales, trimestrales y mensuales, para ello se selecciono de la información proporcionada por la API CoinGecko de la cual se seleccionó el precio, capitalización de mercado, volumen total y fecha (price, market_cap, total_volume, date) información necesaria para los KPIs a implementar.

SE CARGÓ LA INFORMACION HISTORICA SOLO EN DOLARES AMERICANOS DESDE ARCHIVOS DE LA API COINGECKO

# INFORMACION CARGADA DE LA API COINGECKO : 5 AÑOS TOMADOS DEL 2018/8/9 AL 2023/8/9 SON 1796 DIAS 
 CARGAMOS LA INFORMACION HISTORICA SOLO EN DOLARES AMERICANOS 

Abrimos un archivo historico por cada criptomoneda que viene en formato JSON y lo pasamos a Pandas
para depurarlo y le agragamos el id.

Los archivos en formato JSON son: market_bitcoin, market_binancecoin, market_cardano, market_dogecoin, 
market_ethereum, market_polkadot, market_ripple, market_solana, market_tether, market_uniswap.

Se crean 10 archivos depurados en formato csv, uno por cada criptomoneda, a los cuales se les convierte el timestand que es fecha en formato UNIX a formato fecha YYYY-MM-DD y se le 
agrega el campo id.

Este el el archivo que tiene el EDA del proyecto:
EDA_criptomonedas_P102.ipynb

Luego se hace un analisis visual utilizando la libreria matplotlib (import matplotlib.pyplot as plt) por cada archivo de criptomoneda, usando plt.figure

EDA para la criptomoneda binancecoin (siymbol BNB) se nota una informacion limpia consistente, sin outliers, la curva ascendente de las graficas corresponde al  omportamiento de crecimiento de la moneda en los ultimos años y en cuanto a volumenes totales su comportamiento es muy estables, reflejando la realidad de la moneda.

EDA para la criptomoneda bitcoin (siymbol BTC) se nota una informacion limpia consistente, sin outliers, los picos de valorizacion corresponde al comportamiento pico de la moneda en 2022 luego la caida moderada en 2023.

EDA para la criptomoneda cardano (siymbol  ADA) se nota una informacion limpia consistente, sin outliers los aumentos de finales del 2021 son los comportamientos reales de la criptomoneda en esos meses.

EDA para la criptomoneda dogecoin (siymbol DOGE) se nota una informacion limpia consistente, sin outliers el pico de 2021 año donde tuvo su mayor crecimiento, refleja el movimiento de la cripto que decrecio para 2022 y continua con un comportamiento estable hasta la fecha

EDA para la criptomoneda ethereum (siymbol ETH) se nota una informacion limpia consistente, sin outliers comportamiento muy parecido al bitcoin con un pico de crecimiento en 2021 y con una estabilidad desde 2022 a la fecha.

EDA para la criptomoneda polkadot (siymbol DOT) se nota una informacion limpia consistente, sin outliers, el pico del 2021 muy comun en todas las criptos y desde julio de 2022  a la fecha un comportamiento muy estable.

EDA para la criptomoneda ripple (siymbol XRP)  se nota una informacion limpia consistente, sin outliers, los picos de 2021 reflejan la realidad de la cripto, muy similar a todas las criptos analizadas y con un comportamiento estable desde junio de 2022 a la fecha.

EDA para la criptomoneda solana (siymbol SOL) se nota una informacion limpia consistente, sin outliers, comportamiento esperado, se aprecia un pico en 2021 y desde junio de 2022 a la fecha un comportamiento estable.

EDA para la criptomoneda tether (siymbol USDT) se nota una informacion limpia consistente, sin outliers, precio estable a lo largo del tiempo, con un pico en volúmenes en 2021,  y con un alto volumen.

EDA para la criptomoneda uniswap (siymbol UNI) se nota una informacion limpia consistente, sin outliers, refleja un comportamiento estable desde el segundo semestre de 2022 y el pico de 2021 muy comun en todas las criptos analizadas.

DESPUES DE ANALIZAR CADA CRIPTOMOMEDA SE CONCATENAN LOS 10 ARCHIVOS CORRESPONDIENTES A LAS CRIPTOMONEDAS.

Luego se crea la lista de criptomonedas que contenga id, symbol y name desde el archivo de descripcion de crptomonedas de la API CoinGecko, que seria una tabla maestra.

Es Eliminada la columna "platforms", ya que no es necesaria para el análisis.

Paso seguido, se seleccionan del total de monedas, las 10 escogidas para el análisis y se crea el archivo lista_monedas.csv con las 10 criptomonedas a analizar.

# KPIs usados en el Dashboard de POWER BI

1. **Ratio de Capitalización de Mercado a Volumen (Market Cap to Volume Ratio):**  
    Descripción: Es para evaluar la relación entre la capitalización de mercado de una criptomoneda y su volumen de operaciones o trading. Puede ayudar a identificar si una criptomoneda está sobrevalorada o infravalorada en función de la actividad de negociación.

    Fórmula: Ratio de Capitalización de Mercado a Volumen = Capitalización de Mercado / Volumen de Operaciones

2. **Capitalización de Mercado Total (Total Market Capitalization):**
    Descripción: Suma de las capitalizaciones de mercado individuales de todas las criptomonedas en un momento específico.
    
    Fórmula: Total Market Cap = Σ (market_cap) para todas las criptomonedas


3. **Volumen Total de Operaciones (Total Trading Volume):**
    Descripción: Suma de todos los volúmenes de operaciones de todas las criptomonedas durante un período específico.
    
    Fórmula: Total Trading Volume = Σ (total_volume) para todas las criptomonedas

# KPIs Adicionales 

4. **Dominio de Mercado (Market Dominance):**
    Descripción: Calcula la capitalización de mercado de una criptomoneda específica como porcentaje del total del mercado de criptomonedas.
    
    Fórmula: Market Dominance (%) = (Market Cap de una criptomoneda / Total Market Cap) * 100

5. **Crecimiento del Precio (Price Growth):**
    Descripción: Calcula el porcentaje de cambio en el precio de una criptomoneda durante un período específico.
    
    Fórmula: Price Growth (%) = ((Precio final - Precio inicial) / Precio inicial) * 100



