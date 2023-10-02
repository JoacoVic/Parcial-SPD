# ParcialDomiciliario1


## 🧑‍🎓Estudiante
- Joaquín N. Vicente

## Proyecto: Contador de 0 a 99
![parcial_domiciliario_1](https://github.com/JoacoVic/ParcialDomiciliario1/assets/133211768/0439fcaa-f1b0-4a4a-bfa5-1a292e0bb46b)


## Descripción
El proyecto sirve como un contador de 0 a 99 en donde se pueden subir o bajar los valores en unidades. Utiliza 2 displays de 7 segmentos y la técnica de multiplexación.

# Función principal
Esta función se encarga de reconocer el botón que se presionó para cambiar el contador.

```C
int presionarBoton(void)
{
 botonSubir = digitalRead(SUBIR);
 botonBajar = digitalRead(BAJAR);
 botonResetear = digitalRead(RESETEAR);
 if (botonSubir)
   botonSubirPrevio = 1;
 if(botonBajar)
   botonBajarPrevio = 1;
 if(botonResetear)
   botonResetearPrevio = 1;
 
 if (botonSubir == 0 && botonSubir != botonSubirPrevio)
  {
   botonSubirPrevio = botonSubir;
   return SUBIR;
  }
 if (botonBajar == 0 && botonBajar != botonBajarPrevio)
  {
   botonBajarPrevio = botonBajar;
   return BAJAR;
  }
 if (botonResetear == 0 && botonResetear != botonResetearPrevio)
  {
   botonResetearPrevio = botonResetear;
   return RESETEAR;
  }
 return 0;
}
```

## 🤖 Link al proyecto
- [proyecto](https://www.tinkercad.com/things/6vzLoPOFNS7-parcial-domiciliario-spd-joaquin-vicente/editel?sharecode=amWLb_-UNT1qJ1Hg_kgoauOPl_ppTlKQK9IMiE71BLw)





 
