# Impresoras 3D - Configuraciones Optimizadas

Este repositorio contiene configuraciones optimizadas para diferentes impresoras 3D, organizadas por marca y modelo.

## 📁 Estructura del Repositorio

```
impresoras3D/
├── README.md
├── creality-ender-2pro/
│   ├── documentation/
│   │   └── Ender2Pro_OptimalSettings.md
│   └── orca-slicer-configs/
│       ├── Ender2Pro_Printer.json
│       ├── PLA_Ender2Pro_Filament.json
│       ├── Quality_Ender2Pro_Process.json
│       └── Draft_Ender2Pro_Process.json
└── [otras-impresoras]/
```

## 🖨️ Impresoras Disponibles

### ✅ Creality Ender 2 Pro
- **Configuración completa** para Orca Slicer
- **Perfiles optimizados**: Quality y Draft
- **Documentación técnica** completa con explicaciones
- **Velocidades calibradas** específicamente para el frame de Ender 2 Pro
- **Soportes inteligentes** (55° threshold vs configuración stock 45°)

## 🚀 Cómo Usar

### Para Orca Slicer:
1. Navegar a `creality-ender-2pro/orca-slicer-configs/`
2. Importar cada archivo JSON en Orca Slicer:
   - `File → Import → Import Config`
   - Seleccionar archivos JSON uno por uno
3. Usar perfiles:
   - **Printer**: `Creality Ender 2 Pro Optimized`
   - **Filament**: `PLA Ender 2 Pro Optimized`
   - **Process**: `Quality Ender 2 Pro` o `Draft Fast - Ender 2 Pro`

### Documentación:
- Leer `documentation/Ender2Pro_OptimalSettings.md` para entender cada parámetro
- Contiene explicaciones técnicas del "por qué" de cada configuración

## 📊 Resultados vs Configuración Stock

| Métrica | Stock/Genérico | Optimizado | Mejora |
|---------|----------------|------------|---------|
| Outer wall speed | 200mm/s ❌ | 35mm/s ✅ | Calidad superficial |
| Support threshold | 30-45° ❌ | 55° ✅ | 70% menos soportes |
| Support adhesion | Pegado ❌ | 0.7mm XY ✅ | Fácil remoción |
| Tiempo typical | Referencia | -30% ⚡ | Más eficiente |

## 🎯 Filosofía de las Configuraciones

- **Velocidades realistas** para cada impresora específica
- **Soportes inteligentes** - mínimos pero efectivos  
- **Temperaturas calibradas** por tipo de filamento
- **Documentación educativa** - entender el "por qué"
- **Múltiples perfiles** - Quality vs Draft según necesidad

## 🤝 Contribuciones

¿Tienes configuraciones optimizadas para otras impresoras? ¡Contribuye!

1. Crea carpeta con formato: `marca-modelo/`
2. Incluye configuraciones + documentación
3. Sigue la estructura existente
4. Pull request con descripción detallada

---

*Configuraciones basadas en análisis técnico y pruebas reales*
*Actualizado: Septiembre 2025*