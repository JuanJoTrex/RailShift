# 🚆 RailShift

**Calculador de jornadas ferroviarias**

RailShift es una aplicación web sencilla para calcular y cuadrar jornadas de trabajo asociadas a servicios ferroviarios.

La aplicación permite introducir la hora de salida y llegada de un tren y calcula automáticamente la **hora de inicio de jornada**, teniendo en cuenta las **8 horas de trabajo y los 45 minutos de descanso obligatorio**.

## ✨ Características

- 🕐 Cálculo automático de la hora de inicio de jornada.
- 🚆 Introducción de hora de salida y llegada del tren.
- 🌙 Gestión automática de trenes que cruzan la medianoche.
- ⏱️ Jornada calculada de **8 h 45 min**.
- 🧰 Cálculo del tiempo disponible para preparación antes de la salida.
- 📱 Interfaz adaptada para teléfonos móviles.
- 💾 No almacena datos.
- 🌐 Funciona directamente en el navegador.
- 🔌 No necesita servidor ni base de datos.

## 🧮 ¿Cómo funciona?

RailShift calcula la jornada hacia atrás desde la hora de finalización del tren.

La jornada está compuesta por:

```text
8 horas de trabajo
+
45 minutos de descanso
=
8 horas y 45 minutos
```

Por ejemplo:

```text
Salida del tren:    13:30
Llegada del tren:   21:30

21:30 - 8:45 = 12:45
```

Por tanto:

```text
Inicio de jornada:  12:45
Salida del tren:    13:30
Llegada:             21:30
```

### 🌙 Cruce de medianoche

RailShift también detecta automáticamente cuando el tren termina al día siguiente.

Ejemplo:

```text
Salida:             19:00
Llegada:             04:00 (+1 día)
```

El cálculo se realiza desde la llegada:

```text
04:00 - 8:45 = 19:15
```

Resultado:

```text
Inicio de jornada: 19:15 del día anterior
Salida del tren:   19:00
Llegada:            04:00 del día siguiente
```

## 🔒 Privacidad

RailShift no almacena información de los usuarios.

Los horarios introducidos se procesan directamente en el navegador mediante JavaScript y no se envían a ningún servidor.

## 📄 Licencia

Este proyecto puede ser utilizado y modificado según los términos de la licencia definida en este repositorio.
