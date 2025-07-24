---
icon: pen
cover: ../../../.gitbook/assets/tcw-wip-banner.jpg
coverY: 0
---

# Economía Autosostenible

Bla

### El 'Rent' de las _narices_.

El primer obstaculo, que parecia insalvable fue el _rent_ de Solana: resulta que aunque se llame _alquiler_ se ve que es mas bien un _depósito_ o _fianza_ y que normalmente se deposita un **rent equivalente a dos años** para que dicha cuenta se considere '_rent-extemp_'.

> Yo no se como se lo hacen para complicar tanto la explicacion: para cada cosa que despliegas en la red solana, programas, cuentas derivadas, tokens y demas, tienes que pagar las comisiones de red y depositar SOL en dicha cuenta, segun los bytes que almacenes.

Tambien existe el _cierre_ de cuentas **controlado**, que permite recuperar el _rent_; pero esto se tiene que implementar en cada programa de forma especifica.

A demas, como hemos dicho, el _rent_ a depositar en cada cuenta depende del tamaño en bytes: almacenamiento basico y programas simples depositan un rent de unos SOL 0.001141; pero esto escala rapidamente para PDA de almacenamiento de datos, si esto no se optimiza, el almacenamiento de un unico sistema estelar en bruto podria llegar a costar SOL 0.3 o incluso más, haciendo prohibitivo el despliegue de un sector de 500 mundos, e inviable la escala Imperial: 11000 mundos y subiendo.
