# Creality Ender 2 Pro - Configuraciones Optimizadas

Configuraciones específicas para Creality Ender 2 Pro con cama caliente.

## 📁 Contenido

### 📋 Documentación
- `Ender2Pro_OptimalSettings.md` - Guía completa con explicaciones técnicas

### ⚙️ Configuraciones Orca Slicer
- `Ender2Pro_Printer.json` - Perfil de impresora optimizado
- `PLA_Ender2Pro_Filament.json` - Configuración PLA calibrada
- `Quality_Ender2Pro_Process.json` - Perfil principal (0.2mm, balance calidad/tiempo)
- `Draft_Ender2Pro_Process.json` - Perfil rápido para pruebas (0.3mm)

## 🚀 Instalación Rápida

1. **Importar en Orca Slicer**:
   ```
   File → Import → Import Config
   ```
   - Importar los 4 archivos JSON

2. **Seleccionar perfiles**:
   - Printer: `Creality Ender 2 Pro Optimized`
   - Filament: `PLA Ender 2 Pro Optimized`
   - Process: `Quality Ender 2 Pro` (principal) o `Draft Fast` (pruebas)

## ⚡ Mejoras vs Configuración Stock

### Velocidades Corregidas:
- **Outer wall**: 200mm/s → 35mm/s (eliminó vibraciones)
- **Inner wall**: 300mm/s → 45mm/s (velocidad realista)
- **Travel**: 500mm/s → 100mm/s (evita belt slip)

### Soportes Inteligentes:
- **Threshold**: 30° → 55° (70% menos soportes innecesarios)
- **XY distance**: 0.35mm → 0.7mm (fácil remoción)
- **Pattern**: Tree supports (mejor post-procesado)

### Adhesión Mejorada:
- **Primera capa**: 60°C (máxima adhesión)
- **Resto**: 55°C (mantiene sin sobrecargar PSU)
- **Cooling**: Progresivo 0% → 75% (evita warping)

## 📊 Tiempos de Impresión

| Modelo | Quality | Draft | Comparación |
|--------|---------|-------|-------------|
| Pequeño (50x50mm) | 2-4h | 1.5-3h | Draft -25% |
| Mediano (100x100mm) | 6-10h | 4-7h | Draft -30% |
| Grande (150x150mm) | 12-20h | 8-14h | Draft -35% |

## 🎯 Cuándo Usar Cada Perfil

### Quality_Ender2Pro ✅
- Piezas finales/definitivas
- Modelos funcionales
- Superficie visible importante
- Tolerancias dimensionales críticas

### Draft_Ender2Pro ⚡
- Prototipos y pruebas
- Verificación de dimensiones
- Modelos temporales
- Cuando el tiempo es crítico

## 🔧 Especificaciones de la Impresora

- **Área de impresión**: 165 x 165 x 180mm
- **Nozzle**: 0.4mm estándar
- **Extrusor**: Bowden (retracción 5mm)
- **Cama**: Caliente (modificación vs modelo base)
- **Frame**: Ligero (requiere velocidades conservadoras)

## 📖 Documentación Completa

Ver `documentation/Ender2Pro_OptimalSettings.md` para:
- Explicación técnica de cada parámetro
- Cuándo y cómo ajustar configuraciones
- Troubleshooting de problemas comunes
- Mantenimiento recomendado

---

*Configuraciones basadas en análisis de G-code real y pruebas de impresión*