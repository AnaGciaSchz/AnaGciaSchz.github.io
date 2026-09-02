---
title: Cusdis, el sistema de comentarios que prioriza la privacidad
description: ¿Qué es Cusdis? ¿Por qué debería usarlo?
date: "2024-01-18"
image: cover.jpg
tags:
    - recommendation
---

<h3>¿Qué es Cusdis?</h3>

Esa fue mi primera pregunta a la hora de decidir qué tecnología usar para la sección de comentarios de mis posts.

Como dicen en su web, [cusdis.com](https://cusdis.com/):

> **Cusdis** es una **alternativa a Disqus** de código abierto, ligera y centrada en la privacidad. Es muy fácil de usar e integrar con tu web actual. No te rastreamos ni a ti ni a tus usuarios.

¿Y qué es [Disqus](https://disqus.com/about-us/)? Es un sistema de comentarios muy usado en distintas webs y comunidades online, que permite a los usuarios comentar sobre cualquier cosa y participar en discusiones de blogs.

Por supuesto, como orgullosa desarrolladora en [Open Innovation in Privacy](https://oi.empathy.co/#open-privacy), cuando descubrí que existía una tecnología de comentarios similar a una de las más populares, pero con un compromiso real con la privacidad de los usuarios, tuve que elegirla.

<h3>¿Cómo se hostea?</h3>

Al principio, di por hecho que tendría que hostear la tecnología yo misma, pero no fue el caso.

Cusdis ofrece un plan gratuito para hostear un sitio y moderar manualmente hasta cien comentarios al mes, con diez comentarios adicionales que se pueden moderar automáticamente. También puedes pagar 5$/mes para tener sitios y funciones de moderación ilimitados.

![Imagen con los dos planes que ofrece Cusdis actualmente](1.jpg)

<h3>¿Cómo se configura?</h3>

Al registrarte en Cusdis, puedes generar un board para tu sitio y obtener toda la información necesaria.

La plataforma te da el código embebido que necesitas para configurarlo:

![Ejemplo del código embebido y el botón en el Dashboard para conseguirlo](2.jpg)

Si usas la [misma plantilla que yo](https://github.com/CaiJimmy/hugo-theme-stack) en tu web, puedes coger el id de ese código embebido (el valor `data-app-id`) y ponerlo en la configuración (en `config/_default(params.toml`):
```toml
## Comments
[comments]
enabled = true
provider = "cusdis"

[comments.cusdis]
host = "https://cusdis.com"
id = "pasteTheIdHere"
```

<h3>¿Cómo funciona?</h3>

Los comentarios pueden ser anónimos, ya que los usuarios pueden optar por un nombre de usuario aleatorio cada vez que participan. Para mantener un ambiente positivo y seguro, los comentarios no se publican de inmediato.

Como dueña de la página, puedes moderarlos desde el dashboard:

![Vista del Dashboard con un comentario por moderar](3.jpg)

Y no te preocupes por enterarte de cuándo alguien comenta en tu página. Cusdis te avisará por correo electrónico ;)

![Ejemplo de correo notificando un nuevo comentario](4.jpg)

<h3>Conclusión</h3>

Si estás buscando un sistema de comentarios, dale una oportunidad a esta alternativa centrada en la privacidad. No solo es fácil de usar: ¡es una opción fiable y respetuosa!

-----

> Imagen obtenida de [cusdis.com](https://cusdis.com/)
