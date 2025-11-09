# Análisis de necesidades — Landing Page para IPN

Fecha: 2025-11-09

Objetivo: Analizar las necesidades de una landing page orientada a 4 públicos principales (Estudiantes, Padres, Profesionales, Empleadores) y definir objetivos de conversión y recomendaciones prácticas.

## Resumen ejecutivo

La landing debe convertir tráfico en acciones concretas por público: leads para estudiantes, confianza y solicitud de información para padres, captación de profesionales a formación continua y canales de colaboración para empleadores. Debe ser una página estática, accesible y mobile-first con elementos de prueba social (logos, testimonios) y formularios cortos que alimenten un flujo de seguimiento.

Puntos clave:
- Idioma principal: español (considerar versión en inglés si se busca público internacional).
- Trust elements: logos institucionales, acreditaciones, testimonios con foto/rol.
- Flujos: CTA → micro-formulario (3 campos) → email de confirmación automático.
- Métricas: conversiones por CTA, envíos de formularios, tasa de rebote, origen UTM.

## Tabla: Público | Objetivo | CTA principal

| Público       | Objetivo de conversión (qué queremos que haga)                     | CTA principal (texto sugerido)                    |
|---------------|--------------------------------------------------------------------|--------------------------------------------------|
| Estudiantes   | Captar interés y generar lead (inscripción a jornada/solicitud de info) | "Solicita información / Reserva tu visita"       |
| Padres        | Generar confianza y solicitud de información sobre programas y apoyo | "Pide una cita informativa"                      |
| Profesionales | Promover formación continua, diplomados y networking; captar leads   | "Explora cursos para profesionales"              |
| Empleadores   | Facilitar contacto para colaboración, prácticas y contratación       | "Colabora con nosotros / Contacta a empresas"    |

### Notas por público
- Estudiantes: CTA debe llevar a un micro-formulario (máx. 3 campos) + opción de descargar brochure. CTA secundario: "Ver carreras".
- Padres: incluir sección de apoyo estudiantil, becas y testimonios de familias. CTA secundario: "Ver guía para padres".
- Profesionales: destacar oferta de posgrados/diplomados, modalidades y casos de éxito. CTA secundario: "Solicita programa detallado".
- Empleadores: incluir formulario para acuerdos institucionales y botón para publicar oferta de prácticas; mostrar logos de partners.

## Métricas / KPIs recomendados
- Conversiones por CTA (desglosadas por público).
- Tasa de conversión formulario / visitas.
- Time to contact (tiempo de respuesta del equipo a nuevos leads).
- Origen de tráfico (UTM) y coste por lead si se usan campañas.

## Recomendaciones rápidas de contenido y UX
- Hero claro y directo: valor + CTA visible (ej.: "Formación técnica con vínculo industrial — IPN").
- One-page con secciones ancladas para cada público (Estudiantes, Padres, Profesionales, Empleadores).
- Formularios muy cortos y confirmación automática por email con recursos descargables.
- Añadir prueba social prominente (testimonios, logos de empresas), y datos cuantitativos cuando sea posible (no inventar cifras).
- Mobile-first: CTAs grandes, botones y formularios optimizados.

## Sugerencias técnicas iniciales
- Scaffold mínimo a añadir: `index.html`, carpeta `assets/` (CSS minimal, placeholder image), y un `README.md` que explique cómo servir localmente.
- Despliegue simple: GitHub Pages (usar `main` o `gh-pages`) con `index.html` en la raíz o `docs/`.
- Tracking básico: incluir Google Analytics / GA4 o Plausible y recibir eventos de clic en CTAs y envíos de formularios.

## Próximos pasos sugeridos
1. Generar microcopy: 2–3 variantes por CTA para pruebas A/B.
2. Crear scaffold de la landing (HTML + CSS + assets) y desplegar en GitHub Pages.
3. Añadir un formulario que guarde leads en Google Sheets o en un endpoint simple (si se requiere). 
4. Decidir prioridades: ¿idioma, KPI principal (inscripciones vs. leads), presupuesto para ads?

---
Archivo generado automáticamente: `Documentacion/analisis_landing_ipn.md` — si quieres, traduzco el documento al inglés o genero el scaffold ahora.
