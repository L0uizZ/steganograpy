<h1>Steganograpy - Image Steganography Coder</h1>

<h2> about </h2>

<p>steganography is the method of hiding secret data in files.<br>
the idea behind image-based steganography is simple<br>
images are composed of digital data (pixels), which describes what’s inside the picture<br>
usually the colors of all the pixels<br>
every image is made up of pixels and every pixel contains 3-values (red, green, blue)
</p>

<h3>encoding data</h3>
<p>every byte of data is converted to its 8-bit binary code using ASCII values<br>
now pixels are read from left to right in a group of 3 containing a total of 9 values<br>
the first 8-values are used to store binary data<br>
the value is made odd if 1 occurs and even if 0 occurs
</p>

<h3>decoding data</h3>
<p>three pixels are read at a time, till the last value is odd, which means the message is over<br>
every 3-pixels contain a binary data, which can be extracted by the same encoding logic<br>
If the value if odd the binary bit is 1 else 0
</p>

<h2> dependencies </h2>

 1) create virtual environment

         cd steganograpy

         python -m venv venv

         source venv/bin/activate

 2) Pillow - module for editing different image file formats

         pip install Pillow

<h2> run </h2>

 1) run steganograpy

         python steganogra.py

<img src="encoded-img.png" width="50%">
