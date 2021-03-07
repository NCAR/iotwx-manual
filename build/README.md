# Building Your Station

<img width="360" alt="atmos node"
src="https://github.com/NCAR/iotwx-manual/blob/main/img/station-full.jpg"/>

**PARTS LIST**

Before getting started, you should consult the complete list of parts
and hardware that can be found at:

* See the
  [Google spreadsheet](https://drive.google.com/file/d/1lAb784yfsxWOiH-yVCXQ3Ii0yEgUmtUQ/view?usp=sharing)
  for the full, up-to-date list of _non-printed_ parts for building a
  complete station. The vast majority of parts can be found on Amazon,
  through online electronics distributors and through your local
  hardware store.

**Note:** the base case build has quantities preset to 1 item. Also,
**alternative power options** are also listed in this document for users
interested in further customizing their station to specific power needs.

If you only wish to do tabletop testing, you will only need to follow
the [flash instructions](https://github.com/NCAR/iotwx-manual/tree/master/flash) for the microcontroller and then proceed to
the [tabletop testing](#skeletontabletop-testing). This will eliminate
the need for making wiring bundles, constructing a PVC frame or printing
the 3d-printed housing.

## 3D-Printing

All parts can be found in the [stl](./stl) folder and in conjection 
with the station assembly instructions.

Reference stations have been produced with PLA+ material, but
ABS and other materials may be used, provided you have 
enough expertise using them.

## Framing

* [PVC Framing Stand Assembly](./NCAR_PVC_Node_Assembly_Doc.pdf) instruction set

## Wiring

All wiring is based on the Grove / PH2.0-4P which is a 4 pin cable capable of carrying digital, analog and I2C signals.  Grove cables come in buckled and unbuckled styles as well as many sizes from 20cm to 2m.  Grove cables can also be connected directly to GPIOs with both male and female jumper cables.



An assortment of cables can be reliably found here: [Search results for: grove cable – Mouser](https://www.mouser.com/Search/Refine?Keyword=grove+cable).



Long cable (1m - 2m) can be found here: [Unbuckled Grove Cable 1m/2m/50cm/20cm/10cm | m5stack-store](https://m5stack-store.myshopify.com/collections/m5-accessory/products/4pin-buckled-grove-cable)



### Qwicc

There are many Grove sensors provided by SeeedStudio, but another connector standard also exists to open up even more sensors. Deveopled by Sparkfun, [Qwicc](https://www.sparkfun.com/qwiic) is also a 4 pin I2C connector that is capable of being connected to Grove and visa-versa.  If you wish to explore the wide variety of sensors, browse what's possible from [Qwiic Sensors: SparkFun Electronics](https://www.sparkfun.com/categories/399)), [STEMMA/Qwiic Sensors: Adafruit Industries, Unique &amp; fun DIY electronics and kits](https://www.adafruit.com/category/1005), [Qwiic ModulesL Smart Prototyping Zio](https://www.smart-prototyping.com/Zio/zio-modules) and others. 



We have been successful using Adafruit Qwiic digital compass sensors in the AeroNode.



### GPIO Connections

If you want to connect directly to the GPIO (either using the recommended reference microcontroller m5Stack Atom Lite or some other microcontroller), the male and female jumper cables can be used as needed:

* male 4 pin Grove Jumper cable: [110990210 Seeed Studio | Mouser](https://www.mouser.com/ProductDetail/Seeed-Studio/110990210?qs=1%252B9yuXKSi8A2O44lPDM%252BLw%3D%3D)

* female 4 pin Grove Jumper cable: [110990028 Seeed Studio | Mouser](https://www.mouser.com/ProductDetail/Seeed-Studio/110990028?qs=1%252B9yuXKSi8Bgmubyjm2m%2Fw%3D%3D)



## Station Assembly

You can find the various assembly instructions in the provided PDF files:

* [Aero Node Assembly](./NCAR_AERO_Node_Assembly_Doc.pdf) instruction set
* [Hydro Node Assembly](./NCAR_HYDRO_Node_Assembly_Doc.pdf) instruction set
* [Atmos Node Assembly](./NCAR_ATMOS_Node_Assembly_Doc.pdf) instruction set

This is a community driven project, if you would like to contribute proposed changes to the assembly instructions or see other issues please submit it via [New Issues]( https://github.com/NCAR/iotwx-manual/issues)

## Skeleton/Tabletop Testing

The IoTwx system is designed to allow for rapid and flexible testing well _before_ assembly.  In fact, you can set up a system without any frame at all to burn in, test or add new components.



Simply flash the code onto the microcontroller, connect the sensors and you're done.



## Solar Assembly

*coming soon
