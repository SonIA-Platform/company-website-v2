# Guia De Implementacion En Astro

Astro debe producir HTML rapido, accesible y con el minimo JavaScript posible. La web corporativa es principalmente contenido y presentacion; la hidratacion se reserva para interacciones que realmente la necesiten.

## Antes De Tocar Codigo

Revisa:

- `package.json` y scripts;
- `astro.config.*`;
- integraciones instaladas;
- `src/layouts`;
- `src/pages`;
- `src/components`;
- `src/styles`;
- `public`;
- convenciones de naming e imports.

## Estructura De Referencia

```text
src/
  components/
    layout/
    sections/
    ui/
  layouts/
    BaseLayout.astro
  pages/
  styles/
    tokens.css
    global.css
public/
  brand/
  images/
```

No impongas esta estructura si el proyecto ya tiene una arquitectura coherente.

## Tokens Y CSS

- Integra los tokens CSS una sola vez.
- No importes previews, slides ni UI kits al bundle de produccion.
- Usa custom properties del sistema.
- Mobile first.
- Mantén `hover`, `focus-visible`, `active` y `disabled`.
- Respeta `prefers-reduced-motion`.
- Evita `!important` salvo conflicto justificado.

## Componentes

Crea un componente cuando aparece mas de una vez, tiene variantes reales, encapsula una convencion de accesibilidad o centraliza una parte del sistema visual.

No crees abstracciones genericas solo para reducir tres lineas de markup.

## SEO

Cada pagina publica debe tener titulo unico, meta description especifica, `lang="es"`, headings coherentes y contenido principal visible sin JavaScript.

No agregues schema.org con datos inventados.

## Comprobaciones

Ejecuta los scripts disponibles, por ejemplo `npm run build`, `npm run check`, `npm run lint` o `npm test`. No inventes scripts; si no existen, indicalo en el resumen final.
