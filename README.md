# Ecommerce AI Telegram

Pequeño proyecto hecho con n8n para probar un asistente de compras usando OpenAI.

El bot funciona desde Telegram, puede buscar productos, responder consultas y generar pedidos. Además guarda el historial de la conversación en Google Sheets para tener un registro de cada interacción.

## Qué hace

- Recibe mensajes desde Telegram.
- Responde usando OpenAI.
- Busca productos mediante una API.
- Crea pedidos.
- Guarda el historial de conversaciones.
- Mantiene un poco de contexto entre mensajes.

## Cómo funciona

```
Telegram
    │
    ▼
Telegram Trigger
    │
    ▼
AI Agent
 ├── OpenAI
 ├── Memory
 ├── Product Search
 └── Create Order
    │
    ├── Telegram Reply
    └── Google Sheets
```

## Requisitos

- n8n
- OpenAI
- Un bot de Telegram
- Google Sheets

## Importar el workflow

1. Abrí n8n.
2. Importá `workflow.json`.
3. Volvé a conectar las credenciales de:
   - OpenAI
   - Telegram
   - Google Sheets

Las credenciales no están incluidas en el archivo exportado.

## Personalización

Este ejemplo usa la Fake Store API para los productos, pero se puede reemplazar por cualquier API o base de datos.

También se puede cambiar fácilmente:

- el modelo de OpenAI
- el prompt
- el sistema de memoria
- dónde se guardan los pedidos
- el canal de mensajería

## Estructura

```
.
├── README.md
└── workflow.json
```

## Nota

Lo armé como un proyecto para experimentar con agentes de IA en n8n. La idea es tener una base simple sobre la que después se puedan conectar catálogos reales y sistemas de e-commerce.