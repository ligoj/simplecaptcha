# simplecaptcha

A simple captcha repackaged for Jakarta

Based on original code (http://simplecaptcha.sourceforge.net)

Maven dependency

```xml
 <dependency>
   <groupId>org.ligoj</groupId>
   <artifactId>simplecaptcha</artifactId>
   <version>2.0.0</version>
 </dependency>
```

Java usage

``` java
 List<Color> colors = new ArrayList<Color>();
 colors.add(Color.GREEN);
 colors.add(Color.BLUE);
 
 List<Font> fonts = new ArrayList<Font>();
 fonts.add(new Font("Geneva", 2, 32));
 fonts.add(new Font("Courier", 3, 32));
 
 WordRenderer wordRenderer = new DefaultWordRenderer(colors, fonts);
 
 Captcha captcha = new Captcha.Builder(150, 50).addText(wordRenderer)).build();
 
 //Output to file
 CaptchaServletUtil.writeImage(new FileOutputStream("d:\\captcha.png"), captcha.getImage());
 
 //Show it on the web page
 CaptchaServletUtil.writeImage(response, captcha.getImage());
 
```

Samples

![001](example/captcha1.png)

![002](example/captcha2.png)

![003](example_big.png)

![004](example/example_chinese.png)

![005](example/example_multi.png)

![006](example/example_outline_noisy.png)


