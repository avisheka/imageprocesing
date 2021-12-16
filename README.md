# Imageprocesing

# Problem Statement
Need a solution to transcode image type from svg to png & return the base 64 logocontent of the transcoded png image.

# Approach
I tried the following:
1. ImageIO from batik jars for SVG images. Batik helps to raster a svg image. This directly didn't help.
2. twelvemonkey ImageIO - this extends imageIO to support various other image types.

So, the following dependencies are used.
        <dependency>
            <groupId>com.twelvemonkeys.imageio</groupId>
            <artifactId>imageio-batik</artifactId>
            <version>3.2.1</version>
        </dependency>
        <dependency>
            <groupId>org.apache.xmlgraphics</groupId>
            <artifactId>batik-transcoder</artifactId>
            <version>1.14</version>
        </dependency>
        <dependency>
            <groupId>org.apache.xmlgraphics</groupId>
            <artifactId>batik-codec</artifactId>
            <version>1.14</version>
        </dependency>


# Controller
A Rest controller is exposed through with the image processing to transcode a svg image to base64 encoded png image type can be used.
GET /image/svg/{toImageType}/{base64EncodedLogoPath}/{length}/{width}

Currently this supports only for PNG type, but can be extended to transcode anyother type.


