# view- Intégration html/ CSS


## HTML
-header: @include ('header')

-image: dans le dossier publique

## header + footer = template
### template.blade.php

(header)

@yield('contenu')

(footer)

### page qui contient le header et footer 

@extends ('template')

@section ('contenu')

blablabla

@endsection


## Loop

@foreach(blablabla)

contenu 

@endforeach

(ex)

 @foreach ($products as $product)
        <div class="product">
        <a href='{{ $product->id }}'>

            <div class="image">
                <img src="{{ $product->image }}">
            </div>
            <div class="namePrice">
                <h2>{{ $product->name }}</h2>
                <p>{{ $product->price }} €</p>

            </div>
            </a>
        </div>

    @endforeach
    
    ## Affiher élement d'un tableau
    
    (ex) <h2>{{ $product[0]->name }}</h2>
    
    ## Mettre route dans une view :/ex
    
    <td><a href="{{ url('product/'.$product->id) }}"><button type="button" class="btn btn-success">View</button></a></td>











