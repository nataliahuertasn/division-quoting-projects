# División de cotizaciones y proyectos — mockup de Project Agenda

Mockup navegable (front-end únicamente) de una extensión de **Project Agenda** que permite
clasificar por **División** cada **Scope** de una cotización y crear después **proyectos separados por división**.

No hay backend, base de datos ni APIs: todos los datos son de ejemplo y se pierden al recargar la página.

## Cómo abrirlo

Es un solo archivo. Basta con abrir `index.html` en el navegador (doble clic).
Usa la fuente Roboto desde Google Fonts, por lo que requiere conexión a internet para verse igual que el diseño original.

## Idea de negocio

```
Cotización → Scopes → División → Proyecto
```

- El estimador crea una cotización y, por cada **Scope**, define su **División** y su **Categoría** (producto).
- Cuando la cotización se gana, quien crea los proyectos asigna cada scope a su proyecto, de modo que
  una misma cotización pueda trabajarse y facturarse por separado según la división.
- El **valor del proyecto** es la suma de los scopes seleccionados, nunca el total de la cotización.

## Módulos del mockup

| Módulo | Qué incluye |
|---|---|
| **Sales › Main Board** | Columnas Bidding, Approval y Follow Up. Menú de tres puntos por tarjeta: pasar de columna, y en Follow Up Archive, Lost, Modify y Awarded. |
| **Sales › Leads** | Pestañas New, On Hold, Approved, Rejected y Modification Requested; scopes por lead; crear, editar y aprobar (genera una cotización en Bidding). |
| **Cotización** | General Information, Costs y pestañas del Quote. Costs organiza la cotización en **scopes** (nombre, división, categoría) con sus ítems; reordenables arrastrando. |
| **Edit Item** | Líneas de materiales, ingeniería, fabricación, etc. con parcial y porcentajes automáticos y tablas de totales (COP/USD, lb/kg). |
| **Awarded** | Flujo *Enter the OC* → *Mark Quote As Awarded*: asignar cada scope a un proyecto existente o crear proyectos nuevos. |
| **Projects › Main Board** | Listado con filtros, tarjetas de balance y formulario *New Project* por scopes (*Save & add new project*). |
| **Detalle de proyecto** | Project Details, Quotes (solo los scopes del proyecto) e Invoices (con estados Billed / In Progress, sin superar el precio del proyecto). |
| **Settings › Set Up** | Divisiones con sus productos (categorías). Alimentan los desplegables de División y Categoría. |

## Notas

- Las cotizaciones en **Bidding** empiezan sin scopes; el estimador los arma desde cero.
- La **categoría** pertenece al scope; los ítems la heredan y no se edita en el formulario del ítem.
- Interfaz pensada para escritorio y alineada con la estética existente de Project Agenda.
