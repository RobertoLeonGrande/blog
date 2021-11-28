---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# esto es como el head en html
# se ponen las variables que queramos
layout: page # este siempre hay que tenerlo, son las plantillas
tittle: Blog El molino de Frades
menu: Inicio
description: La historia del molino de Frades
permalink: / # enlace permanente que no es el normal, en este caso se refiere al directorio

# de las tres lineas para abajo es el contenido de la pagina
---
<section> <!-- Para secionar contenidos diferentes-->
    <div class="section-title"><h2>Ultimas entradas</h2></div>
    <div class="section-post-list post-list"> <!--el post-list afecta a todas las etiquetas que estan debajo de la llamada-->
        <ul>
        {% for post in site.posts %}<!-- carga los elementos indicados-->
            <li class="post-list-item">
                <a href="{{ post.url | relative_url }}"><img src="{{ post.media | relative_url }}"  alt="Imagen no disponible"/></a>
                <a href="{{ post.url | relative_url }}"><h3>{{ post.title }}</h3></a>
                <p>{{ post.assert }}</p>
            </li>
        {% endfor %}
        </ul>
    </div>
</section>
