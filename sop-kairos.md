SOP: Desarrollo de Dashboard de Gestión de Pedidos y Finanzas - Tienda Floral
Rol de la IA: Senior Full Stack Developer & UX/UI Designer. Objetivo: Crear un Dashboard intuitivo y visualmente atractivo que fusione la gestión de estados de pedido (Kanban) con el control de saldos financieros en tiempo real.

1. Definición de Stack Tecnológico y Estética
Framework: React.js o Next.js con Tailwind CSS.

Componentes: Framer Motion (para transiciones suaves) y Lucide React (iconografía).

Estilo Visual: "Sofisticado Oscuro". Paleta de colores: Fondos en Carbón Profundo (#1A1A1A) o Negro Suave, con acentos en Dorado (#D4AF37) y Blanco Puro.
    
    Logo: Uso del isotipo (símbolo) exclusivamente, omitiendo el texto "Kairos".
    
    Tipografía: Inter o Montserrat para máxima legibilidad, con pesos ligeros para elegancia.

2. Arquitectura de la Interfaz (Módulos 1 y 2 Combinados)
El dashboard debe presentar una vista híbrida donde la métrica financiera sea inseparable de la tarjeta del pedido.

A. Header de Métricas Rápidas:

Card "Flujo de Caja": Total Recaudado vs Pendiente por Cobrar.

Card "Operaciones": Pedidos Críticos (Entregas en < 2h).

B. Sistema de Tarjetas (Kanban Cards): Cada tarjeta de pedido debe incluir:

Visual: Miniatura de la referencia floral.

Identificador: Nombre del cliente y hora de entrega.

Indicador de Pago Dinámico:

Badge con progreso: $ Pagado / $ Total.

Color dinámico: Rojo (0%), Naranja (<100%), Verde (Saldado).

Acciones rápidas: Botón de "Registrar Abono" y "Cambiar Estatus".

3. Lógica de Negocio y Estados
Estados del Kanban:

Validación: Pedidos recién ingresados sin pago confirmado.

Taller: Pedidos con al menos 50% de anticipo (Estado: "En Elaboración").

Logística: Pedidos liquidados al 100% o con acuerdo de pago contra entrega (Estado: "Listo/En Ruta").

Regla de Validación: Impedir el movimiento de una tarjeta a "En Ruta" si el saldo pendiente es > 0, a menos que se active un "Bypass" de confianza.

4. Requerimientos de UX (Interacción)
Drag & Drop: Implementar dnd-kit o react-beautiful-dnd para mover pedidos entre columnas.

Quick View: Al hacer clic en una tarjeta, abrir un Drawer lateral derecho con el detalle del pedido, comprobante de pago adjunto y notas de dedicatoria.

Filtros: Capacidad de filtrar por "Solo deudores" o "Entregas de la mañana".

5. Prompt de Ejecución Inicial
"Actúa como un Senior Full Stack. Genera el código para un componente de Dashboard en React utilizando Tailwind CSS. Necesito una vista de Tablero Kanban donde cada tarjeta represente un pedido floral. Cada tarjeta debe mostrar visualmente si el cliente debe dinero mediante una barra de progreso de pago. La estética debe ser elegante y limpia, enfocada en una dueña de negocio floral. Prioriza la claridad visual sobre el estado financiero de cada pedido."

6. Catálogo de Productos (Definido por Usuario)
    *   **Bouquet & Vino**: Botella con la etiqueta definitiva + Ramo en papel coreano. (Estética: Elegante, minimalista).
    *   **Palomitas**: Bolsa pouch negra con ventana + Etiqueta redonda al centro. (Estética: Textura crujiente visible, empaque mate).
    *   **Brownies**: 3 piezas en caja con tapa de acetato + Lazo de satín. (Estética: Gourmet, brillo del chocolate).
    *   **Pretzels**: Tubo transparente o bolsa con sello de marca. (Estética: Contraste chocolate/sal).
    *   **Paquete "Mini"**: Caja rígida abierta: Mini botella + Mini snacks + Papel seda. (Estética: Abundancia visual, "unboxing").