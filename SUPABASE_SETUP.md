# Configuración de Supabase para tu sitio de crowdfunding

## Paso 1: Crear cuenta en Supabase

1. Ve a https://supabase.com
2. Crea una cuenta gratuita
3. Crea un nuevo proyecto
4. Guarda tu contraseña de base de datos (la necesitarás)

## Paso 2: Obtener las credenciales

1. En tu dashboard de Supabase, ve a **Settings** → **API**
2. Copia:
   - **Project URL** (ejemplo: https://tuproyecto.supabase.co)
   - **anon public** key (la clave pública)

## Paso 3: Configurar las variables de entorno

Crea un archivo `.env` en la raíz de tu proyecto con:

```
VITE_SUPABASE_URL=https://tuproyecto.supabase.co
VITE_SUPABASE_ANON_KEY=tu_clave_publica_aqui
```

## Paso 4: Crear las tablas en Supabase

Ve a **SQL Editor** en tu dashboard y ejecuta este SQL:

```sql
-- Tabla para RSVPs (Confirmaciones de asistencia)
CREATE TABLE rsvps (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  nombre TEXT NOT NULL,
  email TEXT NOT NULL,
  asistira BOOLEAN NOT NULL,
  num_invitados INTEGER NOT NULL DEFAULT 1,
  restricciones_alimentarias TEXT,
  cancion_favorita TEXT,
  mensaje_especial TEXT,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT TIMEZONE('utc', NOW())
);

-- Tabla para Donaciones
CREATE TABLE donaciones (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  experiencia_id TEXT NOT NULL,
  nombre TEXT NOT NULL,
  email TEXT NOT NULL,
  monto DECIMAL(10,2) NOT NULL,
  metodo_pago TEXT NOT NULL,
  mensaje TEXT,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT TIMEZONE('utc', NOW())
);

-- Habilitar Row Level Security (RLS)
ALTER TABLE rsvps ENABLE ROW LEVEL SECURITY;
ALTER TABLE donaciones ENABLE ROW LEVEL SECURITY;

-- Políticas para permitir INSERT público (solo escritura)
CREATE POLICY "Permitir insertar RSVPs públicamente"
ON rsvps FOR INSERT
TO anon
WITH CHECK (true);

CREATE POLICY "Permitir insertar donaciones públicamente"
ON donaciones FOR INSERT
TO anon
WITH CHECK (true);

-- Opcional: Política para que solo tú puedas ver los datos
-- (Accede con tu cuenta de Supabase)
CREATE POLICY "Permitir leer RSVPs autenticado"
ON rsvps FOR SELECT
TO authenticated
USING (true);

CREATE POLICY "Permitir leer donaciones autenticado"
ON donaciones FOR SELECT
TO authenticated
USING (true);
```

## Paso 5: Integrar procesador de pagos

Para aceptar donaciones reales, necesitas integrar un procesador de pagos:

### Opción 1: Stripe (Recomendado)
1. Crea cuenta en https://stripe.com
2. Obtén tus API keys de prueba
3. Instala: `npm install @stripe/stripe-js`
4. Sigue la documentación: https://stripe.com/docs

### Opción 2: Mercado Pago
1. Crea cuenta en https://www.mercadopago.com.mx
2. Obtén tus credenciales
3. Sigue la documentación: https://www.mercadopago.com.mx/developers

### Opción 3: PayPal
1. Crea cuenta business en https://www.paypal.com/mx/business
2. Obtén API credentials
3. Usa PayPal SDK: https://developer.paypal.com/

## Paso 6: Implementar notificaciones por email

Para recibir emails cuando alguien done o confirme asistencia:

1. En Supabase, ve a **Database** → **Triggers**
2. O usa servicios como:
   - SendGrid
   - Mailgun
   - Resend

## Paso 7: Desplegar tu sitio

### Opción recomendada: Vercel
1. Sube tu código a GitHub
2. Ve a https://vercel.com
3. Conecta tu repositorio
4. Agrega las variables de entorno (VITE_SUPABASE_URL, VITE_SUPABASE_ANON_KEY)
5. Deploy automático! 🎉

### Alternativa: Netlify
Similar a Vercel, muy fácil de usar.

## Ver datos en tiempo real

1. Ve a tu dashboard de Supabase
2. **Database** → **Tables**
3. Verás todos los RSVPs y donaciones en tiempo real
4. Puedes exportar a CSV o Excel

## Seguridad importante

⚠️ **NUNCA compartas tu SUPABASE_SERVICE_ROLE_KEY** - solo usa la anon key pública
⚠️ Las variables de entorno con `VITE_` son públicas - está bien para la anon key
⚠️ Para producción, configura bien las políticas de RLS en Supabase

## Soporte adicional

- Documentación de Supabase: https://supabase.com/docs
- Canal de Discord de Supabase
- Tutorial de integración de pagos: https://docs.stripe.com/payments/quickstart
