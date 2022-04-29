#QUE ME PONGO - PRIMERA ITERACIÓN

DIAGRAMA DE CLASES

![Diagrama QMPv2](https://user-images.githubusercontent.com/69949020/163748407-b26f4807-4191-40bf-a1ba-6d60de77b313.png)


PSEUDOCODIGO

enum CategoriaPrenda{

    ACCESORIOS,
    PARTE_SUPERIOR,
    PARTE_INFERIOR,
    CALZADO
}

enum Material{
    ALGODON,
    LANA,
    SEDA,
    FIBRA_SINTETICA
}

enum TipoPrenda{

    abstract CategoriaPrenda getCategoria()

    ANTEOJOS{@override getCategoria(){return ACCESORIOS}},
    REMERA_MANGA_CORTA{@override getCategoria(){return PARTE_SUPERIOR}},
    PANTALON{@override getCategoria(){return PARTE_INFERIOR}},
    CROCS{@override getCategoria(){return CALZADO}}
}


Class Prenda{

    TipoPrenda tipoPrenda
    Material materialPrenda
    Color colorPrincipal
    Color colorSecundario

    Prenda(TipoPrenda tipo, Material material, Color colorPrimario){
        this.tipoPrenda = requireNonNull(tipo,"El tipo de una prenda es obligatorio");
        this.materialPrenda = requireNonNull(material,"El material de una prenda es obligatorio");
        this.colorPrincipal = requireNonNull(colorPrimario,"El color Principal de una prenda es obligatorio");
    }

    void setColorSecundario(Color color){
        this.colorSecundario = color;
    }

    CategoriaPrenda getCategoria{
        return tipo.getCategoria()
    }    
    
}
