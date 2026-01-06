# 💍 Página de Boda - Sil & Boo

Página web de crowdfunding para celebrar nuestra boda el **21 de Noviembre, 2026** en el Salón Los Ángeles, Ciudad de México.

---

## 🎨 Características

- ✨ **Hero personalizado** con ilustración de la pareja y sus mascotas
- 💕 **Nuestra Historia** - Relato emotivo de cómo nos conocimos
- 📅 **Detalles de la celebración** con fecha, hora y ubicación
- 🗺️ **Google Maps integrado** para llegar al Salón Los Ángeles
- 🎁 **6 Experiencias** para que los invitados contribuyan
- 💳 **Sistema de donaciones SPEI** (transferencias bancarias)
- 📝 **RSVP funcional** conectado a Supabase
- 📱 **100% responsive** - Optimizado para mobile
- 🎯 **Economía conductual** - Prueba social, urgencia, anclaje de precio

---

## 🚀 Publicación Rápida

### Desde Figma Make:

**NUEVO:** Si estás en Figma Make, lee esta guía primero:
- 📥 [`INICIO_RAPIDO_FIGMA_MAKE.md`](./INICIO_RAPIDO_FIGMA_MAKE.md) - 15 minutos
- 📘 [`GUIA_FIGMA_MAKE_A_VERCEL.md`](./GUIA_FIGMA_MAKE_A_VERCEL.md) - Guía completa

### Opción Recomendada: Vercel (GRATIS)

1. **Lee la guía rápida:** [`QUICK_START.md`](./QUICK_START.md)
2. **Sigue 3 pasos simples:** GitHub → Vercel → Compartir
3. **Tiempo total:** 10 minutos
4. **Costo:** $0 USD

---

## 📚 Documentación

| Archivo | Descripción |
|---------|-------------|
| [`QUICK_START.md`](./QUICK_START.md) | 🚀 Publica en 10 minutos |
| [`DEPLOY_INSTRUCTIONS.md`](./DEPLOY_INSTRUCTIONS.md) | 📘 Guía completa de publicación |
| [`HOSTING_ALTERNATIVES.md`](./HOSTING_ALTERNATIVES.md) | 🌐 Comparación de opciones de hosting |
| [`MOBILE_OPTIMIZATION.md`](./MOBILE_OPTIMIZATION.md) | 📱 Guía de optimización mobile |
| [`PRE_LAUNCH_CHECKLIST.md`](./PRE_LAUNCH_CHECKLIST.md) | ✅ Checklist antes de lanzar |

---

## 🛠️ Stack Tecnológico

- **Frontend:** React 18 + TypeScript
- **Styling:** Tailwind CSS v4
- **Build:** Vite
- **Backend:** Supabase (PostgreSQL)
- **Hosting:** Vercel (recomendado)
- **Payments:** Transferencias SPEI (Stori Bank)

---

## 🎨 Paleta de Colores

```css
/* Colores principales */
--rojo-principal: #BE3E3E    /* Botones, acentos, amor */
--beige-acento: #E8D7C6      /* Íconos, detalles suaves */
--azul-hero: #4F61FB          /* Fondo hero section */
--negro-botones: #2C2C2C     /* Botones de experiencias */

/* Tipografía */
--titulo: 'Playfair Display', serif   /* Elegante, emotivo */
--cuerpo: 'Inter', sans-serif         /* Legible, moderno */
```

---

## 📂 Estructura del Proyecto

```
/
├── src/
│   ├── app/
│   │   ├── App.tsx                    # Componente principal
│   │   └── components/
│   │       ├── ExperienceCard.tsx     # Tarjeta de experiencia
│   │       ├── DonationModal.tsx      # Modal de donaciones
│   │       ├── RsvpModal.tsx          # Modal de RSVP
│   │       ├── OurStory.tsx           # Sección historia
│   │       ├── WeddingDetails.tsx     # Detalles evento
│   │       └── ThankYouNotification.tsx
│   ├── lib/
│   │   └── supabase.ts                # Cliente Supabase
│   ├── styles/
│   │   ├── theme.css                  # Tokens de diseño
│   │   └── fonts.css                  # Fuentes personalizadas
│   └── imports/                       # Imágenes de Figma
├── vercel.json                        # Config Vercel
├── package.json                       # Dependencias
└── [DOCUMENTACIÓN]                    # Guías de deploy
```

---

## 🗄️ Base de Datos (Supabase)

### Tablas:

#### `rsvps`
```sql
- id: UUID (PK)
- nombre: TEXT
- email: TEXT
- asistira: BOOLEAN
- num_invitados: INTEGER (1 o 2)
- restricciones_alimentarias: TEXT
- cancion_favorita: TEXT
- mensaje_especial: TEXT
- created_at: TIMESTAMP
```

#### `donaciones`
```sql
- id: UUID (PK)
- experiencia_id: TEXT
- nombre: TEXT
- email: TEXT
- monto: INTEGER
- metodo_pago: TEXT ('transferencia_spei')
- mensaje: TEXT
- created_at: TIMESTAMP
```

---

## 💳 Datos Bancarios

**Banco:** Stori  
**Titular:** Juan Carlos Jimenez Espinosa  
**CLABE:** 646180402300001416  
**Entidad:** STP  

---

## 🌐 URLs Importantes

| Recurso | URL |
|---------|-----|
| **Pinterest (código vestimenta)** | https://mx.pinterest.com/silvanacoami/boda-sil-y-boo/ |
| **Salón Los Ángeles** | Google Maps integrado |
| **Fecha:** | 21 de Noviembre, 2026 |
| **Hora:** | 5:00 PM |

---

## 📱 Mobile-First

Esta página fue diseñada con **Mobile First** en mente:

- ✅ Responsive breakpoints (sm, md, lg)
- ✅ Touch-friendly buttons (mínimo 44x44px)
- ✅ Formularios optimizados para mobile
- ✅ Modales que funcionan en pantallas pequeñas
- ✅ Tipografía escalable
- ✅ Imágenes optimizadas

**Vercel agrega automáticamente:**
- Compresión WebP
- Lazy loading
- CDN global
- HTTP/2 y HTTP/3

---

## 🎯 Características UX

### Economía Conductual:
- **Prueba social:** "18 personas ya ayudaron"
- **Escasez:** "💕 Casi Completo"
- **Anclaje de precio:** Montos sugeridos
- **Progreso visible:** Barras de progreso por experiencia
- **Urgencia temporal:** "Confirma antes del 1 de Noviembre"

### Personalización:
- Tono cálido y cercano
- Historia emotiva del origen
- Nombres de las mascotas incluidos
- Experiencias únicas y personales

---

## 🔐 Variables de Entorno

Crea un archivo `.env` local con:

```bash
VITE_SUPABASE_URL=tu_url_de_supabase
VITE_SUPABASE_ANON_KEY=tu_clave_anonima
```

**IMPORTANTE:** 
- NO subas el archivo `.env` a GitHub (ya está en `.gitignore`)
- En Vercel, agrégalas en: Settings → Environment Variables

---

## 🚀 Comandos

```bash
# Instalar dependencias
npm install

# Desarrollo local
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview
```

---

## 📊 Performance

### Objetivos:

| Métrica | Mobile | Desktop |
|---------|--------|---------|
| Performance | >80 | >90 |
| Accessibility | >90 | >90 |
| Best Practices | >90 | >95 |
| SEO | >90 | >95 |

**Core Web Vitals:**
- LCP: <2.5s
- FID: <100ms
- CLS: <0.1

---

## 🎉 Experiencias Disponibles

1. 🗾 **Luna de Miel Japón** - $80,000 MXN
2. 💆‍♂️ **Día de Spa** - $2,500 MXN
3. 🎨 **Tour de Museos CDMX** - $1,800 MXN
4. 🐕 **Road Trip con los Perritos** - $4,000 MXN
5. 🍷 **Cena de Aniversario** - $3,000 MXN
6. 💃 **Salón Los Ángeles 2.0** - $1,500 MXN

---

## 📞 Soporte

- **Vercel Docs:** https://vercel.com/docs
- **Supabase Docs:** https://supabase.com/docs
- **Tailwind CSS:** https://tailwindcss.com/docs
- **React:** https://react.dev

---

## ✨ Créditos

**Diseño y Desarrollo:** Figma Make + IA  
**Ilustraciones:** Personalizadas de la pareja  
**Tipografía:** Google Fonts (Playfair Display, Inter)  
**Hosting:** Vercel  
**Backend:** Supabase  

---

## 📝 Licencia

Proyecto personal - Boda de Sil & Boo  
© 2024-2026. Todos los derechos reservados.

---

## 💕 Agradecimientos

Gracias a todos nuestros invitados y colaboradores que harán posible estos sueños.

**¡Nos vemos en la pista de baile! 💃🕺**

---

## 🔗 Links Rápidos

- 🚀 **[Guía de Publicación Rápida](./QUICK_START.md)**
- 📘 **[Instrucciones Completas](./DEPLOY_INSTRUCTIONS.md)**
- 🌐 **[Opciones de Hosting](./HOSTING_ALTERNATIVES.md)**
- 📱 **[Optimización Mobile](./MOBILE_OPTIMIZATION.md)**
- ✅ **[Checklist Pre-Lanzamiento](./PRE_LAUNCH_CHECKLIST.md)**

---

**¡Hecho con 💕 para celebrar el amor!**