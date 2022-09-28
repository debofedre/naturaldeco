DESAFÍO SASS

1- Agregué un extend en la línea 106 de main.scss.
Afecta el texto dentro de la imagen fija en el index.

p{
        @extend h3;
        padding-top: 0;
    }

2- Agregué un mixin en la línea 244 y 282 de main.scss.
Afecta el tamaño de los iconos de las redes del footer y el sticky.

@mixin sizes ($width, $height){
    width: $width;
    height: $height;
}
/*Sticky Whatsaap*/
.stickyBtn{
    position: fixed;
    bottom: 30px;
    right:20px;
    z-index: 1000;
    a{
    img{
        @include sizes (60px, 60px)
        }
    }
}

/*Mixin*/
@mixin sizes ($width, $height){
    width: $width;
    height: $height;
}
.redes img{
    @include sizes (40px, 40px);
    margin-right: 10px;
    transition: all 0.2s ease-in-out;
    &:hover{
        transform: scale(0.8);
    }
}

3-Agregué un map en la línea 318 de main.scss.
Cambia el fondo de los iconos de las esencias en el index.

/*Map*/
/*keys / Values*/
$esencias:(
    tilo: #90B77D,
    lavanda: #898AA6,
    melissa: #42855B,
);

@each $key, $value in $esencias{
    .map--#{$key}{
        &:hover{
            background-color: $value;
            border-radius: 50%;
        }
    }
}

DESAFÍO SEO

1-Agregué un meta description y un meta keywords en todos los html