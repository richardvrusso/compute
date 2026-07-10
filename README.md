<style>
  table {
    border-collapse: collapse !important;
    width: 100%;
    margin-bottom: 20px;
  }
  th, td {
    border: 1px solid #224422 !important; /* Faint matrix-green lines to match the Hacker theme */
    padding: 10px !important;
  }
  /* Force all images in the first column to be exact 60x60 pixel squares */
  td:first-child img {
    width: 300px !important;
    height: 300px !important;
    object-fit: contain !important; /* Prevents the image from stretching or distorting */
    background-color: transparent;  /* Keeps it clean on the dark background */
</style>

# unRAID Compute Server
Taking a play from my enterprise world. This is a compute server only running Docker and VMs.

| Preview | Product Name | Component Specifications & Notes |
| :---: | :--- | :--- |
| ![Case](https://m.media-amazon.com/images/I/91UOdM9izhL._AC_SL1500_.jpg) | [Cooler Master MasterBox Q300L Micro-ATX Tower](https://a.co/d/06zHDARY){:target="_blank"} | Micro-ATX form factor case layout |
| ![Motherboard](https://c1.neweggimages.com/productimage/nb1280/13-183-597-04.jpg) | [SUPERMICRO X10SRM-F Micro ATX Server Motherboard R3](https://www.newegg.com/supermicro-x10srm-f-single-socket-r3-support-intel-xeon-processor-e5-2600-v4-v3-e5-1600-v4-v3/p/N82E16813183597){:target="_blank"} | LGA 2011 Intel C612 chip platform |
| ![CPU](https://m.media-amazon.com/images/I/41C5WTFh9zL._AC_.jpg) | [Intel Xeon E5-2650 V4 Processor (Renewed)](https://a.co){:target="_blank"} | SR2N3 12-Core 2.2GHz 30MB Cache LGA 2011-3 |
| ![RAM](https://m.media-amazon.com/images/I/61Ag5zLT3pL._AC_SL1250_.jpg) | [SK HYNIX 32GB PC4-19200T-R Server Memory](https://a.co/d/03uwxJMB){:target="_blank"} | HMA84GR7MFR4N-UH DDR4-2400 ECC RDIMM 2Rx4<br>• *128GB total setup of ECC RAM* |
| ![SSD](https://m.media-amazon.com/images/I/81iA+O1AnrL._AC_SL1500_.jpg) | [Toshiba KXG60ZNV256G NVMe M.2 SSD](https://a.co){:target="_blank"} | 3MM Height 80MM Length Single Sided TLC<br>• *2 for a mirrored cache to run Docker/VMs* |
| ![SSD](https://m.media-amazon.com/images/I/51nnZ+cziYL._AC_SL1080_.jpg) | [Crucial P3 1TB Gen3 3D NAND NVMe M.2 SSD](https://a.co){:target="_blank"} | High speed data layer drive<br>• *Cache dedicated to downloads/extractions* |
| ![SSD](https://m.media-amazon.com/images/I/51tIK96OB+L._AC_SL1280_.jpg) | [Intel SSD DC S4500 1.92TB Enterprise SSD](https://a.co/d/01J4x3ZY){:target="_blank"} | 3D TLC SATA 6Gb/s 2.5-Inch drive tier<br>• *1 drive for array overflow protection if cache fills* |
| ![Fan](https://m.media-amazon.com/images/I/71cTdx43gNL._AC_SL1500_.jpg) | [be quiet! Shadow Wings 2 120mm PWM Fan](https://a.co){:target="_blank"} | Silent low noise chassis cooling fan<br>• *Front and rear fans for the case* |
| ![Cooler](https://m.media-amazon.com/images/I/8170Uni2LxL._AC_SL1500_.jpg) | [Noctua NH-D9DX i4 3U Premium CPU Cooler](https://a.co){:target="_blank"} | High performance heatsink for Intel Xeon LGA20xx |
| ![Heatsink](https://m.media-amazon.com/images/I/51tXCRhCKAL._AC_SL1000_.jpg) | [M.2 2280 SSD Heatsink Block](https://a.co){:target="_blank"} | Thermal management accessory<br>• *Attached to the download M.2 drive* |
| ![Heatsink](https://m.media-amazon.com/images/I/61-ANLVDGaL._SL1500_.jpg) | [GLOTRENDS M.2 Heatsink for 2280 SSD](https://a.co){:target="_blank"} | Aluminum cooling fin plate<br>• *Attached to the dual app/VM M.2 drives* |
| ![Adapter](https://m.media-amazon.com/images/I/61V+KdwQwNL._AC_SL1500_.jpg) | [10Gtek 2-Port M.2 NVMe Adapter](https://a.co/d/00sMVUkL){:target="_blank"} | Dual drive interface slot device<br>• *Holds the two 256GB M.2 drives for apps/VMs* |
| ![Adapter](https://m.media-amazon.com/images/I/71+b6ucVA6L._AC_SL1500_.jpg) | [GLOTRENDS PA09-HS M.2 NVMe to PCIe 4.0 X4](https://a.co){:target="_blank"} | Expansion storage adapter with built-in heatsink<br>• *Holds the M.2 for download extraction* |
| ![NIC](https://m.media-amazon.com/images/I/51HsviUQa7L._AC_.jpg) | [MellanoxConnectX-3 EN 10G Ethernet SFP+ PCI-E NIC](https://a.co){:target="_blank"} | High speed data backbone fiber interface network card<br>• *Connects to SFP in a Ubiquiti 24-port POE switch* |
| ![Cable](https://m.media-amazon.com/images/I/51SK0aIAJhL._SL1008_.jpg) | [H!Fiber.com 2 Pack 10G SFP+ DAC Cable 2M](https://a.co){:target="_blank"} | Twinax passive network patch link assemblies<br>• *One for unRAID server and one for storage server* |
| ![PSU](https://m.media-amazon.com/images/I/71BtdBtKX5L._AC_SL1500_.jpg) | [Thermaltake Toughpower GX2 600W ATX PSU](https://a.co){:target="_blank"} | 80+ Gold certified continuous power delivery unit |
