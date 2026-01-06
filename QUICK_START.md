# 🚀 Guía Rápida: Publica tu Página en 10 Minutos

## ⚡ OPCIÓN MÁS RÁPIDA: VERCEL (100% GRATIS)

### 📋 Resumen:
- ✅ **Costo:** $0 USD (gratis para siempre)
- ✅ **Tiempo:** 10 minutos
- ✅ **Optimización mobile:** Automática
- ✅ **Duración:** Ilimitada (hasta Nov 2026 y más allá)
- ✅ **Velocidad:** CDN global (rápido en todo México)

---

## 🎯 3 PASOS SIMPLES

### ▶️ PASO 1: Sube tu código a GitHub (5 min)

#### Opción A: GitHub Desktop (MÁS FÁCIL) ⭐

1. **Descarga GitHub Desktop:**
   - Ve a: https://desktop.github.com
   - Descarga e instala

2. **Crea cuenta en GitHub:**
   - Ve a: https://github.com
   - Sign Up (gratis)

3. **Publica tu proyecto:**
   - Abre GitHub Desktop
   - File → Add Local Repository
   - Selecciona la carpeta de tu proyecto
   - Click en "Publish repository"
   - Nombre: `boda-sil-boo`
   - ✅ Desmarcar "Keep this code private" (o déjalo privado)
   - Click "Publish Repository"

**✅ ¡Listo! Tu código está en GitHub.**

---

#### Opción B: Terminal (Para usuarios avanzados)

```bash
# En la carpeta de tu proyecto:
git init
git add .
git commit -m "Initial commit"

# Crea repo en github.com/new, luego:
git remote add origin https://github.com/TU_USUARIO/boda-sil-boo.git
git branch -M main
git push -u origin main
```

---

### ▶️ PASO 2: Publica en Vercel (3 min)

1. **Ve a Vercel:**
   - https://vercel.com

2. **Sign Up:**
   - Click "Sign Up"
   - Selecciona "Continue with GitHub"
   - Autoriza la conexión

3. **Importa tu proyecto:**
   - Click "Add New..." → "Project"
   - Busca "boda-sil-boo" en la lista
   - Click "Import"

4. **Configura (déjalo como está):**
   - Framework Preset: `Vite` (detectado automáticamente)
   - Build Command: `npm run build`
   - Output Directory: `dist`

5. **Agrega variables de entorno (IMPORTANTE):**
   - Click "Environment Variables"
   - Agrega:
     ```
     VITE_SUPABASE_URL = [tu URL de Supabase]
     VITE_SUPABASE_ANON_KEY = [tu clave anónima]
     ```
   
   **¿Dónde los encuentro?**
   - supabase.com → Tu proyecto → Settings → API
   - Copia "Project URL" y "anon public key"

6. **Deploy:**
   - Click "Deploy"
   - ☕ Espera 2-3 minutos

**✅ ¡Tu página está publicada!**

---

### ▶️ PASO 3: Comparte el Link (2 min)

Tu página estará en:
```
https://boda-sil-boo.vercel.app
```

O el nombre que hayas elegido.

**¡Ya puedes compartir este link con tus invitados!** 🎉

---

## 📱 WhatsApp: Mensaje de Invitación

Copia y pega este mensaje:

```
¡Nos casamos! 💕

Sil & Boo
📅 21 de Noviembre, 2026
🕐 5:00 PM
📍 Salón Los Ángeles, CDMX

🎉 Confirma tu asistencia aquí:
[PEGA TU LINK DE VERCEL]

¡Nos vemos en la pista de baile! 💃🕺

```

---

## 📸 Instagram: Post de Invitación

```
¡Nos casamos! 💍✨

📅 21 de Noviembre, 2026
📍 Salón Los Ángeles

🔗 Link en bio para confirmar asistencia

#BodaSilYBoo #21Nov2026 #SalonLosAngeles #CDMX
```

---

## 🔄 ¿Necesitas Actualizar tu Página?

Cada vez que hagas cambios en tu código:

### Con GitHub Desktop:
1. Abre GitHub Desktop
2. Verás tus cambios listados
3. Escribe mensaje: "Actualizar [lo que cambiaste]"
4. Click "Commit to main"
5. Click "Push origin"
6. **Vercel detecta el cambio automáticamente**
7. ⏰ En 2-3 minutos, tu página se actualiza

**¡Así de fácil!** 🎯

---

## 💰 COSTO TOTAL

| Concepto | Precio |
|----------|--------|
| **Hosting en Vercel** | **$0 USD** ✅ |
| **GitHub** | **$0 USD** ✅ |
| **Supabase** | **$0 USD** ✅ |
| **SSL/HTTPS** | **$0 USD** ✅ |
| **CDN Global** | **$0 USD** ✅ |
| **Optimización Mobile** | **$0 USD** ✅ |
| **TOTAL** | **$0 USD** 🎉 |

**Dominio personalizado (opcional):** $200-300 MXN/año

---

## ✅ Checklist Rápido

Antes de compartir, verifica:

- [ ] Página carga en: `https://______.vercel.app`
- [ ] Fecha correcta: 21 de Noviembre, 2026
- [ ] Datos bancarios correctos (CLABE)
- [ ] Botón RSVP funciona
- [ ] Botón "Regalar Experiencia" funciona
- [ ] Probado en tu celular
- [ ] Supabase guardando datos

---

## 🆘 Solución de Problemas

### ❌ "Build failed" en Vercel
**Solución:** Verifica las variables de entorno (VITE_SUPABASE_URL y VITE_SUPABASE_ANON_KEY)

### ❌ "No puedo ver mi repositorio en Vercel"
**Solución:** En Vercel, autoriza el acceso a tus repositorios de GitHub

### ❌ "Supabase no funciona"
**Solución:** 
1. Ve a Vercel → Settings → Environment Variables
2. Verifica que las 2 variables estén correctas
3. Redeploy (Deployments → ⋯ → Redeploy)

### ❌ "La página tarda mucho en cargar"
**Solución:** Vercel optimiza automáticamente. Espera 5 minutos después del primer deploy.

---

## 📚 Documentación Completa

Si necesitas más detalles, revisa:

- 📘 `DEPLOY_INSTRUCTIONS.md` - Guía paso a paso detallada
- 🌐 `HOSTING_ALTERNATIVES.md` - Comparación de opciones
- 📱 `MOBILE_OPTIMIZATION.md` - Optimización mobile
- ✅ `PRE_LAUNCH_CHECKLIST.md` - Checklist completo

---

## 🎉 ¡ESO ES TODO!

En solo **10 minutos**, tu página de boda estará en línea, optimizada y lista para compartir con el mundo.

**¡Felicidades y que disfruten su boda! 💕**

---

## 🔗 Links Útiles

| Servicio | URL |
|----------|-----|
| **Vercel** | https://vercel.com |
| **GitHub** | https://github.com |
| **GitHub Desktop** | https://desktop.github.com |
| **Supabase** | https://supabase.com |
| **PageSpeed Test** | https://pagespeed.web.dev |
| **Mobile Test** | https://search.google.com/test/mobile-friendly |

---

**¿Listo para publicar? ¡Vamos!** 🚀
