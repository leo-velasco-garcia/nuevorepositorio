<template>
    <BodyHdos text="Movimiento"/>
    <BodyHtres text="Físicas" ident="fisicas"/>
    <BodyP text="Hemos escogido unas curvas de velocidad que transmitan los valores y el tono de la marca. Para ello hemos decidido utilizar un movimiento ease out con velocidad de salida 76% y velocidad de entrada 16%." />

    <BodyImagen text="/movimiento/COSAS PARA MANUAL CESIDA-53.png" />
    <BodyHtres text="Sistema" ident="sistema"/>
    <BodyHcuatro text="Tipos de entrada" />
    <BodyHcinco text="Entrada de rotación de derecha a izquierda" />
    <BodyP text="Este primer tipo de entrada se determina haciendo un salto de escala de 0 a 100%, que a su vez se combina con una rotación de derecha a izquierda y de 0 a -90°." />
    <BodyHcinco text=" Entrada de rotación de izquierda a derecha" />
    <BodyP text=" Teniendo en cuenta que no todas las animaciones iban a entrar por el mismo lado de la pantalla se determinó esta variante de entrada para sustituir a la primera en caso de que entre por la izquierda de la pantalla. Se ejecuta con una escala de 0 a 100% y una rotación de izquierda a derecha y de 0 a 90°." />
    <BodyHcinco text="Entrada recta de derecha a izquierda" />
    <BodyP text="Esta entrada fue otro tipo de solución para algunas animaciones que era más aconsejable quitar el movimiento principal para que no entorpeciese en la legibilidad. Se recrea con un posicionamiento basado en el espacio de keyframes determinado por si es una animación grande o pequeña." />
    <BodyHcinco text=" Entrada recta de izquierda a derecha" />
    <BodyP text="Variación de la entrada anterior, cambiando el posicionamiento de izquierda a derecha." />

    
    <BodyHcuatro text="Tipos de salida" />
    <BodyP text="Una vez animada la entrada se determinó como deberían finalizar las animaciones, para ello se crearon dos tipos de salidas que se pueden complementar con los diferentes tipos de entrada." />
    <BodyHcinco text="Salida por opacidad" />
    <BodyP text="Se utiliza cuando la animación entra con las variantes de rotación de izquierda a derecha o derecha a izquierda. Su funcionamiento explicado en el manual ofrece un desvanecimiento de opacidad de 100 a 0%." />
    <BodyHcinco text="Salida por plano" />
    <BodyP text="Se complementa con las entradas rectas de la marca, se crea con la distancia de fotogramas establecidos en el manual, en los que la unidad básica desaparece de la pantalla con un movimiento de posición con las curvas ajustadas." />

    <BodyHtres text="Timing" ident="timing"/>
    <BodyP text="Se nos planteó el problema de las velocidades aplicadas en función al tamaño y la visibilidad en pantalla según diferentes animaciones, la respuesta a este problema fué plantear diferentes timings en función al formato de la animación que se vaya a plantear." />
    <BodyHcuatro text=" Animación de formato grande" />
    <BodyP text="Para las animaciones de grandes dimensiones como por ejemplo la formación del logo se estableció que el movimiento de la posición de los keyframes debería de estar separado por 13 fotogramas cada keyframe, además de aplicar las curvas correspondientes del sistema audiovisual." />
    <BodyHcuatro text="Animación de formato pequeño" />
    <BodyP text="En este caso el principal ejemplo es la mosca en el cuál se determinó que el espacio entre keyframes de posición debía de ser 8 fotogramas ya que este tipo de animaciones deben ir más rápido por el tipo de animación que és y el espacio que ocupa en la pantalla." />

    <BodyHtres text="Muestras" ident="muestras"/>
    <BodyHcinco text="Formación de Imagotipo"/>
    <BodyHcinco text="Mosca"/>
    <BodyHcinco text="Sobreimpresión"/>
    <BodyHcinco text="Nombre y Cargo"/>
    <BodyHcinco text="Separador"/>
    <BodyHcinco text="Copyright"/>
    <BodyHcinco text="Cierre"/>
</template>