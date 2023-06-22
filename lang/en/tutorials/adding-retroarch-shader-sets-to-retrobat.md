# Adding RetroArch Shader Sets to Retrobat

Retrobat comes bundled with a set of shaders, however it does not include all shaders available in Retroarch.



You can manually add new Shader Sets to the Retrobat menu for libretro cores, here is the procedure.

<div align="left">

<figure><img src="https://i.imgur.com/XR6pMX0.png" alt=""><figcaption></figcaption></figure>

</div>

## Location of Shaders

### Retrobat

Shaders available in Retrobat are located in the `\system\shaders\configs` folder of your Retrobat installation.

<div align="left">

<figure><img src="https://i.imgur.com/ChxJMdd.png" alt=""><figcaption></figcaption></figure>

</div>

### RetroArch

Shaders available in Retroarch are located in the `\retroarch\shaders\` folder of your Retrobat installation.

They are sorted first by type of shader (glsl or slang):

* GLSL: Shader format available to OpenGL.
* Slang: New and recommended shader format, when available. Compatible with Vulkan, Direct3D 10/11/12, OpenGL Core.

{% hint style="info" %}
Retrobat will automatically search in the right folder based on the video driver defined for the system.
{% endhint %}

Example of shader folders for GLSL:

<div align="left">

<figure><img src="https://i.imgur.com/ijn2wYK.png" alt=""><figcaption></figcaption></figure>

</div>



## Adding a new Shader in the Retrobat menu

Let's say you want to add the Shader "advcartoon" to Retrobat, the shader is available both for GLSL and SLANG:

| ![](<../.gitbook/assets/image (17).png>) | ![](<../.gitbook/assets/image (41).png>) |
| ---------------------------------------- | ---------------------------------------- |

The shader is located in the `\retroarch\shaders\shaders_xxxx\cel` folder and is named "advcartoon.glslp".

To add it to Retrobat, go to the `\system\shaders\configs` folder and create a new folder, name it for example "advcartoon":

<div align="left">

<figure><img src="https://i.imgur.com/xkrY1en.png" alt=""><figcaption></figcaption></figure>

</div>

Inside this folder, create a file called "**rendering-defaults.yml**":

<div align="left">

<figure><img src="https://i.imgur.com/oNGcd2L.png" alt=""><figcaption></figcaption></figure>

</div>

Open the file with your notepad and add the following text:

```yaml
default:
  shader: <retroarch shader folder>/<shader filename without extension>
```

In our example it will be:

```yaml
default:
  shader: cel/advcartoon
```

<div align="left">

<figure><img src="https://i.imgur.com/uKOVcK3.png" alt=""><figcaption></figcaption></figure>

</div>

The shader set will now appear in Retrobat:

<div align="left">

<figure><img src="https://i.imgur.com/J6fPEFF.png" alt=""><figcaption></figcaption></figure>

</div>
