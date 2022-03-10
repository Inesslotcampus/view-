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


