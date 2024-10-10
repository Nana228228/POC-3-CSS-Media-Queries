# POC 3: CSS Media Queries


[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!--índice-->
<p align="center">
  <a href="#introdução">Introdução</a> •
  <a href="uso">Como usar?</a> •
  <a href="#conceitos">Conceitos</a> •
  <a href="print">Impressão</a>•
  <a href="dispositivos">Dispositivos</a>•
  <a href="disposicao">Disposição</a>•
  <a href="autores">Autores</a>•
</p>

<h2 id="introdução">Introdução</h2>
Bem-vindo ao repositório CSS Media Queries! 🎉 O objetivo aqui é oferecer à comunidade um recurso educativo gratuito e acessível para quem deseja aprender ou aprimorar suas habilidades em desenvolver páginas web adaptativas usando media queries do CSS. 

<h2 id="uso">Como usar?</h2>

1. Clone este repositório:
   ```bash
   git clone https://github.com/Nana228228/POC-3-CSS-Media-Queries
   
2. Abra o arquivo index.html no seu navegador para visualizar como a página se adapta a diferentes dispositivos e orientações.

3. Use as ferramentas de desenvolvedor do navegador para simular diferentes resoluções de tela e veja as media queries em ação.

<h2 id="conceitos">Conceitos Iniciais</h2>
As media queries são um recurso do CSS usado para aplicar estilos diferentes a elementos de uma página web, dependendo das características do dispositivo ou ambiente em que a página está sendo visualizada. São fundamentais para o design responsivo, pois permitem ajustar o layout e melhorar a experiência do usuário em dispositivos como smartphones, tablets, desktops, e até para impressão.

<h3>Para que servem:</h3>
-Adaptar o design da página a diferentes tamanhos de tela e dispositivos. <br>
-Aplicar estilos específicos para diferentes resoluções, orientações (retrato vs. paisagem) e condições do dispositivo (por exemplo, para impressão). <br>
-Garantir que a interface seja intuitiva e visualmente agradável em diversos contextos. <br>

<h3>Sintaxe</h3>

```
@media not|only mediatype and (media feature) and (media feature) {
    /* Regras CSS aplicadas se a condição for verdadeira */
    seletor {
        propriedade: valor;
    }
}

```

obs: O mediatype é opcional (se omitido, será definido para todos). No entanto, se você usar not ou only, você também deve especificar um mediatype.


<h2 id="">Media Querie para Impressão </h2>
Para especificar a aparência da página ao ser impressa, usa-se a mediatype print. Há elementos que servem para interatividade com o usuário que não fazem sentido na versão impressa, por exemplo, a navbar. Assim, no exemplo abaixo, optou-se por retirá-la usando o mediatype print:

```
@media print {
            nav {
                display: none;
            }

            .gallery {
                grid-template-columns: repeat(2, 1fr);
            }
        }

```


<h2 id="">Adaptação à Dispositivos com Diferentes Larguras</h2>
No código desse repositório, usou-se uma abordagem mobile first (em que o CSS é escrito inicialmente para dispositivos móveis, e as media queries são usadas para adaptar o layout a dispositivos maiores, como tablets e desktops). Nesse caso, a escolha do mobile first em detrimento do desktop first foi arbitrária. Obs: o media type para mobile (com condição max-width: 600px) foi escrito por fins didáticos, mas poderia ter sido omitido.

```

        /* Media query para smartphones */
        @media (max-width: 600px) {
            nav ul {
                flex-direction: column;
            }

            .gallery {
                grid-template-columns: 1fr;
            }
        }

        /* Media query para tablets */
        @media (min-width: 601px) and (max-width: 900px) {
            .gallery {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* Media query para desktops */
        @media (min-width: 901px) {
            .gallery {
                grid-template-columns: repeat(3, 1fr);
            }
        }

```



<h2 id="">Adaptação Conforme a Disposição do Dispositivo</h2>
Para especificar a aparência da página em diferentes orientações, usa-se a media feature orientation, cujos valores são landscape ou viewport:

```
/* Orientação landscape */
        @media (orientation: landscape) {
            body {
                background-color: #f0f0f0;
            }

            .gallery {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        /* Orientação portrait */
        @media (orientation: portrait) {
            body {
                background-color: #fff;
            }

            .gallery {
                grid-template-columns: repeat(2, 1fr);
            }
        }

```

<h2 id="autores"> Autores </h2>

<h3>Naomi Arakaki</h3>



[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/naomi-suguimoto-57436b290/)](https://www.linkedin.com/in/naomi-suguimoto-57436b290)

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&link=mailto:arakakinaomi228@gmail.com)](mailto:arakakinaomi228@gmail.com)


<h3>Gabriel Aboboreira</h3>


[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/gabriel-aboboreira/)](https://www.linkedin.com/in/gabriel-aboboreira/)

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&link=mailto:masterkillbr007@gmail.com)](mailto:masterkillbr007@gmail.com)


<h3>Ana Julia Blande</h3>


[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white&link=https://www.linkedin.com/in/ana-julia-blande-silva-348612286/)](https://www.linkedin.com/in/ana-julia-blande-silva-348612286/)

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&link=mailto:anajblande04@gmail.com)](mailto:anajblande04@gmail.com)
