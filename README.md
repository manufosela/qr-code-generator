# QRCode Generator

QRCodeGenerator ES6 class.

## Use
```javascript
const qr = new QRCodeGenerator(typeNumber, errorCorrectLevel);
```

Where:
* **typeNumber**: from 1 to 10
  * qrcode size: **1 to max 14 characters** with Low errorCorrectLevel
  * qrcode size: **10 to max 213 characters** with Low errorCorrectLevel

* **errorCorrectLevel**: it can be:
  * **L** (Low)       => **~7%**
  * **M** (Medium)    => **~15%**
  * **Q** (Quartile)  => **~25%**
  * **H** (High)      => **~30%**

## Example
```javascript
  const qr = new QRCodeGenerator(4, 'M');
  const text = "https://manufosela.es";
  qr.addData(text);
  qr.make();
  qrcodeHTML = qr.createImgTag();

  document.querySelector('#qr').innerHTML = qrcodeHTML;
```