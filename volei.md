---
title: volei
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.23"

---

# volei

Base URLs:

* <a href="https://dev.meili.com">Develop Env: https://dev.meili.com</a>

# Authentication

# jogador

## GET jogadores

GET /api/jogadores

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|sexo|query|string| no |none|
|order_by|query|string| no |none|
|sort_by|query|string| no |none|
|posicao|query|string| no |none|
|idade[gte]|query|integer| no |none|
|idade[lte]|query|integer| no |none|
|page|query|integer| no |none|
|perPage|query|integer| no |none|

> Response Examples

> 200 Response

```json
[
  {
    "id": 0,
    "nome": "string",
    "sexo": "string",
    "posicao": "string",
    "idade": 0,
    "bio": "string"
  }
]
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|*anonymous*|[[jogador](#schemajogador)]|false|none||none|
|» id|integer|true|read-only||none|
|» nome|string|true|none||none|
|» sexo|string|true|none||'|
|» posicao|string|true|none||none|
|» idade|integer|true|none||none|
|» bio|string|true|none||none|

## POST criar jogador

POST /api/jogadores

> Body Parameters

```json
{
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[jogador](#schemajogador)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[jogador](#schemajogador)|

## GET jogador por id

GET /api/jogadores/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[jogador](#schemajogador)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|none|Inline|

### Responses Data Schema

HTTP Status Code **404**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» type|string|true|none||none|
|» errors|object|true|none||none|
|»» code|string|true|none||none|
|»» datail|string|true|none||none|

## PUT editar jogador

PUT /api/jogadores/{id}

> Body Parameters

```json
{
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|body|body|[jogador](#schemajogador)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[jogador](#schemajogador)|

## DELETE deletar jogador

DELETE /api/jogadores/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 202 Response

```json
{
  "id": 0,
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|202|[Accepted](https://tools.ietf.org/html/rfc7231#section-6.3.3)|none|[jogador](#schemajogador)|

# arena

## GET arenas

GET /api/arenas

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|tipo_arena|query|string| no |none|
|order_by|query|string| no |none|
|sort_by|query|string| no |none|
|page|query|integer| no |none|
|perPage|query|string| no |none|
|preco_hora[gte]|query|integer| no |none|
|preco_hora[lte]|query|string| no |none|

> Response Examples

> 200 Response

```json
[
  {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  }
]
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|*anonymous*|[[arena](#schemaarena)]|false|none||none|
|» id|integer|true|read-only||ID|
|» tipo_arena|string|true|none||none|
|» nome_arena|string|true|none||none|
|» preco_hora|number|true|none||none|
|» endereco|string|true|none||none|

## POST criar arena

POST /api/arenas

> Body Parameters

```json
{
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[arena](#schemaarena)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[arena](#schemaarena)|

## GET arena por id

GET /api/arenas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[arena](#schemaarena)|

## PUT editar arena

PUT /api/arenas/{id}

> Body Parameters

```json
{
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|body|body|[arena](#schemaarena)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[arena](#schemaarena)|

## DELETE deletar arena

DELETE /api/arenas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 202 Response

```json
{
  "id": 0,
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|202|[Accepted](https://tools.ietf.org/html/rfc7231#section-6.3.3)|none|[arena](#schemaarena)|

# pelada

## GET pelada

GET /api/peladas

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|horario_inicio[gte]|query|number| no |none|
|horario_inicio[lte]|query|number| no |none|
|tipo_jogo|query|string| no |none|
|qtd_horas|query|integer| no |none|
|arena|query|string| no |none|
|id_responsavel|query|integer| no |none|
|page|query|integer| no |none|
|perPage|query|integer| no |none|
|order_by|query|string| no |none|
|sort_by|query|string| no |none|

> Response Examples

> 200 Response

```json
[
  {
    "id": 0,
    "id_responsavel": 0,
    "horario_inicio": "string",
    "tipo_jogo": "string",
    "qtd_horas": 0,
    "arena": {
      "id": 0,
      "tipo_arena": "string",
      "nome_arena": "string",
      "preco_hora": 0,
      "endereco": "string"
    },
    "convites": [
      {
        "id_jogador": 0,
        "status": true
      }
    ]
  }
]
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|*anonymous*|[[pelada](#schemapelada)]|false|none||none|
|» id|integer|true|read-only||ID|
|» id_responsavel|integer|true|none||none|
|» horario_inicio|string|true|none||none|
|» tipo_jogo|string|true|none||none|
|» qtd_horas|integer|true|none||none|
|» arena|[arena](#schemaarena)|true|none||none|
|»» id|integer|true|read-only||ID|
|»» tipo_arena|string|true|none||none|
|»» nome_arena|string|true|none||none|
|»» preco_hora|number|true|none||none|
|»» endereco|string|true|none||none|
|» convites|[object]|true|none||none|
|»» id_jogador|integer|true|none||none|
|»» status|boolean|true|none||none|

## POST criar pelada

POST /api/peladas

> Body Parameters

```json
{
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[pelada](#schemapelada)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[pelada](#schemapelada)|

## GET pelada por id

GET /api/peladas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[pelada](#schemapelada)|

## PUT editar pelada

PUT /api/peladas/{id}

> Body Parameters

```json
{
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|body|body|[pelada](#schemapelada)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[pelada](#schemapelada)|

## DELETE deletar pelada

DELETE /api/peladas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 202 Response

```json
{
  "id": 0,
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|202|[Accepted](https://tools.ietf.org/html/rfc7231#section-6.3.3)|none|[pelada](#schemapelada)|

## POST Ingressar pelada

POST /api/peladas/{id}/ingressar/{id_jogador}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|id_jogador|path|integer| yes |none|

> Response Examples

> 204 Response

```json
null
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|none|null|

## DELETE sair pelada

DELETE /api/peladas/{id}/ingressar/{id_jogador}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|id_jogador|path|integer| yes |none|

> Response Examples

> 204 Response

```json
null
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|none|null|

## GET obter jogadores

GET /api/peladas/{id}/jogadores/

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 200 Response

```json
[
  {
    "status": true,
    "jogador": {
      "id": 0,
      "nome": "string",
      "sexo": "string",
      "posicao": "string",
      "idade": 0,
      "bio": "string"
    }
  }
]
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|boolean|true|none||none|
|» jogador|[jogador](#schemajogador)|true|none||none|
|»» id|integer|true|read-only||none|
|»» nome|string|true|none||none|
|»» sexo|string|true|none||'|
|»» posicao|string|true|none||none|
|»» idade|integer|true|none||none|
|»» bio|string|true|none||none|

# partida

## GET partidas

GET /api/partidas

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|sort_by|query|string| no |none|
|order_by|query|string| no |none|
|page|query|string| no |none|
|perPage|query|string| no |none|

> Response Examples

> 200 Response

```json
[
  {
    "id": 0,
    "tempo_jogo": 0,
    "times": {
      "casa": {
        "pontuacao": 0,
        "jogadores": [
          {
            "id": null,
            "nome": null,
            "sexo": null,
            "posicao": null,
            "idade": null,
            "bio": null
          }
        ]
      },
      "visitante": {
        "pontuacao": 0,
        "jogadores": [
          {
            "id": null,
            "nome": null,
            "sexo": null,
            "posicao": null,
            "idade": null,
            "bio": null
          }
        ]
      }
    },
    "id_pelada": 0
  }
]
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|*anonymous*|[[partida](#schemapartida)]|false|none||none|
|» id|integer|true|read-only||ID|
|» tempo_jogo|number|true|none||none|
|» times|object|true|none||none|
|»» casa|object|true|none||none|
|»»» pontuacao|integer|true|none||none|
|»»» jogadores|[[jogador](#schemajogador)]|true|none||none|
|»»»» id|integer|true|read-only||none|
|»»»» nome|string|true|none||none|
|»»»» sexo|string|true|none||'|
|»»»» posicao|string|true|none||none|
|»»»» idade|integer|true|none||none|
|»»»» bio|string|true|none||none|
|»» visitante|object|true|none||none|
|»»» pontuacao|integer|true|none||none|
|»»» jogadores|[[jogador](#schemajogador)]|true|none||none|
|»»»» id|integer|true|read-only||none|
|»»»» nome|string|true|none||none|
|»»»» sexo|string|true|none||'|
|»»»» posicao|string|true|none||none|
|»»»» idade|integer|true|none||none|
|»»»» bio|string|true|none||none|
|» id_pelada|integer|true|none||none|

## POST criar partida

POST /api/partidas

> Body Parameters

```json
{
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[partida](#schemapartida)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[partida](#schemapartida)|

## GET partida por id

GET /api/partidas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[partida](#schemapartida)|

## PUT editar partida

PUT /api/partidas/{id}

> Body Parameters

```json
{
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|
|body|body|[partida](#schemapartida)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": 0,
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[partida](#schemapartida)|

## DELETE deletar partida

DELETE /api/partidas/{id}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer| yes |none|

> Response Examples

> 0 Response

```json
{
  "id": 0,
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|0|Unknown|none|[partida](#schemapartida)|

# Data Schema

<h2 id="tocS_jogador">jogador</h2>

<a id="schemajogador"></a>
<a id="schema_jogador"></a>
<a id="tocSjogador"></a>
<a id="tocsjogador"></a>

```json
{
  "id": 0,
  "nome": "string",
  "sexo": "string",
  "posicao": "string",
  "idade": 0,
  "bio": "string"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer|true|read-only||none|
|nome|string|true|none||none|
|sexo|string|true|none||'|
|posicao|string|true|none||none|
|idade|integer|true|none||none|
|bio|string|true|none||none|

<h2 id="tocS_pelada">pelada</h2>

<a id="schemapelada"></a>
<a id="schema_pelada"></a>
<a id="tocSpelada"></a>
<a id="tocspelada"></a>

```json
{
  "id": 0,
  "id_responsavel": 0,
  "horario_inicio": "string",
  "tipo_jogo": "string",
  "qtd_horas": 0,
  "arena": {
    "id": 0,
    "tipo_arena": "string",
    "nome_arena": "string",
    "preco_hora": 0,
    "endereco": "string"
  },
  "convites": [
    {
      "id_jogador": 0,
      "status": true
    }
  ]
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer|true|read-only||ID|
|id_responsavel|integer|true|none||none|
|horario_inicio|string|true|none||none|
|tipo_jogo|string|true|none||none|
|qtd_horas|integer|true|none||none|
|arena|[arena](#schemaarena)|true|none||none|
|convites|[object]|true|none||none|
|» id_jogador|integer|true|none||none|
|» status|boolean|true|none||none|

<h2 id="tocS_arena">arena</h2>

<a id="schemaarena"></a>
<a id="schema_arena"></a>
<a id="tocSarena"></a>
<a id="tocsarena"></a>

```json
{
  "id": 0,
  "tipo_arena": "string",
  "nome_arena": "string",
  "preco_hora": 0,
  "endereco": "string"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer|true|read-only||ID|
|tipo_arena|string|true|none||none|
|nome_arena|string|true|none||none|
|preco_hora|number|true|none||none|
|endereco|string|true|none||none|

<h2 id="tocS_partida">partida</h2>

<a id="schemapartida"></a>
<a id="schema_partida"></a>
<a id="tocSpartida"></a>
<a id="tocspartida"></a>

```json
{
  "id": 0,
  "tempo_jogo": 0,
  "times": {
    "casa": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    },
    "visitante": {
      "pontuacao": 0,
      "jogadores": [
        {
          "id": 0,
          "nome": "string",
          "sexo": "string",
          "posicao": "string",
          "idade": 0,
          "bio": "string"
        }
      ]
    }
  },
  "id_pelada": 0
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer|true|read-only||ID|
|tempo_jogo|number|true|none||none|
|times|object|true|none||none|
|» casa|object|true|none||none|
|»» pontuacao|integer|true|none||none|
|»» jogadores|[[jogador](#schemajogador)]|true|none||none|
|» visitante|object|true|none||none|
|»» pontuacao|integer|true|none||none|
|»» jogadores|[[jogador](#schemajogador)]|true|none||none|
|id_pelada|integer|true|none||none|

