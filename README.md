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

enum MaterialPrenda{

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
    MaterialPrenda materialPrenda
    Color colorPrincipal
    Color colorSecundario

    Prenda(TipoPrenda tipo, MaterialPrenda material, Color colorP){
        this.tipoPrenda = tipo != null ? tipo : throw new DomainException("el atributo tipo es obligatorio")
        this.materialPrenda = material != null ? material : throw new DomainException("el atributo material es obligatorio")
        this.colorPrincipal =colorP != null ? colorP : throw new DomainException("el atributo color principal es obligatorio")
    }

    CategoriaPrenda getCategoria{
        return tipo.getCategoria()
    }
    
    
}