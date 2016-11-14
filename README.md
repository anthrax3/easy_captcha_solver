Easy Captcha Solver Gem
----------------
A captcha solver for really easy ones (don't expect it to solve recaptcha or any similar)

Tested on Ruby 2.2

Installation
----------------
gem install 'easy_captcha_solver'


Requirements
----------------

Mac:
* Install Tesseract #=> brew install tesseract
* gem install 'tesseract-ocr'
* gem install 'mechanize'

Ubuntu:
* gem install 'tesseract-ocr'
* gem install 'mechanize'
* export TESSDATA_PREFIX=/usr/share/tesseract-ocr

If eng.traineddata is missing you can download it from : `wget https://github.com/tesseract-ocr/tessdata/raw/master/eng.traineddata`

Tesseract
----------------

This gem uses Tesseract to read captchas, so obviously first of all you will need to install it.

Using the gem
----------------
Solve a captcha using an URL with image_url:

```ruby
require 'easy_captcha_solver'

easy_c = EasyCaptchaSolver.new(image_url: "http://www.madrid.org/infi_pub/html/web/CargarCaptchaAccion.icm?idCaptcha=")
easy_c.captcha #=> "ABCDE"
```
You can also solve a captcha from your local using image_path:

```ruby
require 'easy_captcha_solver'

easy_c = EasyCaptchaSolver.new(image_path: "./captcha_img.jpg")
easy_c.captcha #=> "ABCDE"
```

Contributing
------------
If you'd like to contribute fork the project, make your changes and 
then send a pull request.

Contact
-------
Comments and feedback are welcome.

License
-------
This code is free to use under the terms of the MIT license.


