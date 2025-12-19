# Assets - Imagens

Estrutura para armazenar imagens do site AUTOMATTA.

## Pastas

- **members/** - Fotos dos membros da banda (quadrado, mín. 300x300px)
- **band/** - Imagens gerais da banda (hero, backgrounds, etc)
- **album/** - Capas de álbuns e artwork

## Recomendações

- Usar formatos otimizados: JPEG para fotos, PNG para gráficos
- Manter nomes descritivos em lowercase: `guitarist-name.jpg`
- Comprimir imagens antes de fazer upload (TinyPNG, Optimizilla)
- Tamanho máximo recomendado por arquivo: 500KB

## Como usar no Vue

```vue
<img src="@/assets/images/members/band-member.jpg" alt="Band Member">
```

Ou com import:
```javascript
import memberPhoto from '@/assets/images/members/band-member.jpg'
```
