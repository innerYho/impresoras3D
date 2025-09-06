# CONFIGURACIÓN OPTIMIZADA ENDER 2 PRO
*Configuraciones específicas para Creality Ender 2 Pro con cama caliente*

---

## 🚀 VELOCIDADES OPTIMIZADAS
```
Outer wall speed:        35 mm/s    (Calidad superficial)
Inner wall speed:        45 mm/s    (Balance velocidad/calidad)
Sparse infill speed:     60 mm/s    (Eficiencia)
Solid infill speed:      45 mm/s    (Precisión en capas sólidas)
Top surface speed:       30 mm/s    (Mejor acabado superior)
Support speed:           50 mm/s    (Fácil remoción)
Travel speed:           100 mm/s    (Óptimo para frame Ender 2 Pro)
Initial layer speed:     20 mm/s    (Máxima adhesión)
Small perimeter speed:   25 mm/s    (Detalles finos)
```

## 🌡️ TEMPERATURAS PLA
```
Nozzle temperatura:      205°C      (Primera capa y general)
Bed temperatura:         60°C       (Primera capa)
Bed temperatura resto:   55°C       (Capas siguientes)
```

## 🛠️ SOPORTES INTELIGENTES
```
Support threshold:       55°        (Reduce soportes innecesarios)
Support pattern:         Tree       (Más fácil remoción)
Support density:         15%        (Suficiente resistencia)
Support interface:       2 layers   (Balance adhesión/remoción)
Support XY distance:     0.7mm      (Fácil despegue)
Support Z distance:      0.2mm      (Interface suave)
```

## 📏 CALIDAD Y PRECISIÓN
```
Layer height:            0.2mm      (Balance calidad/velocidad)
First layer height:      0.3mm      (Mejor adhesión)
Line width:              0.4mm      (Nozzle estándar)
Infill density:          15-20%     (Uso general)
Infill pattern:          Cubic      (Resistencia óptima)
```

## 🌀 REFRIGERACIÓN
```
Fan speed primera capa:  0%         (Evita warping)
Fan speed capa 2-3:      25%        (Transición gradual)
Fan speed resto:         75%        (Enfriamiento eficiente)
Bridge fan speed:        100%       (Puentes perfectos)
```

## 🎯 ADHESIÓN Y PRIMERA CAPA
```
Bed adhesion type:       Brim       (Para piezas medianas/grandes)
Brim width:              5mm        (Balance adhesión/desperdicio)
Skirt loops:             3          (Verificar extrusión)
Skirt distance:          6mm        (Espacio seguro)
```

## ⚙️ CONFIGURACIÓN AVANZADA
```
Retraction distance:     5mm        (Bowden tube)
Retraction speed:        45mm/s     (Evita atascos)
Z-hop height:            0.2mm      (Evita arrastre)
Acceleration:            800mm/s²   (Frame ligero)
Jerk (Junction dev):     0.05mm     (Movimientos suaves)
```

## 📦 MATERIALES ESPECÍFICOS

### PLA (Configuración base)
- Nozzle: 200-210°C
- Bed: 50-60°C
- Fan: 75% después capa 3

### PLA+ (Mayor resistencia)
- Nozzle: 210-215°C
- Bed: 60-65°C
- Fan: 50% después capa 3

### PETG (Transparente/flexible)
- Nozzle: 235-245°C
- Bed: 70-75°C
- Fan: 30% después capa 3
- Velocidades: Reducir 25%

## 🔧 MANTENIMIENTO RECOMENDADO

### Antes de cada impresión:
- ✅ Verificar nivelación (papel 0.1mm)
- ✅ Limpiar cama con alcohol isopropílico
- ✅ Verificar tensión correas (pellizco firme)

### Cada 10 impresiones:
- 🔧 Lubricar varillas Z con grasa blanca
- 🔧 Verificar tensión correas
- 🔧 Limpiar extrusor de residuos

### Cada 50 impresiones:
- 🛠️ Calibrar E-steps (stock: ~93)
- 🛠️ Verificar desgaste nozzle
- 🛠️ Limpiar ventiladores

## 🎛️ CONFIGURACIÓN ORCA SLICER

### Crear perfil personalizado:
1. **Printer Settings** → Add Printer → Creality Ender 2 Pro
2. **Modificar dimensiones**: X=165, Y=165, Z=180
3. **Guardar como**: "Ender2Pro_Optimized"

### Filament settings:
1. **Temperature**: Usar valores de arriba
2. **Cooling**: Configurar secuencia gradual
3. **Guardar como**: "PLA_Ender2Pro"

### Process settings:
1. **Speed**: Aplicar todas las velocidades
2. **Support**: Configurar threshold 55°
3. **Guardar como**: "Quality_Ender2Pro"

## 🎮 PERFILES DE CONFIGURACIÓN

### **QUALITY (Configuración principal)**
```
Layer height:     0.2mm     (Balance perfecto calidad/tiempo)
Infill:          15%        (Resistencia estructural adecuada)
Velocidades:     Conserv.   (35-60mm/s - Sin vibraciones)
Soportes:        55°        (Mínimos necesarios)
Tiempo:          100%       (Referencia base)
```
**Usar para**: Piezas finales, modelos funcionales, MacMini definitivo

### **DRAFT (Pruebas rápidas)**
```
Layer height:     0.3mm     (50% menos capas = 50% menos tiempo)
Infill:          10%        (Mínimo estructural para pruebas)
Velocidades:     Rápidas    (50-80mm/s - Límite seguro Ender 2 Pro)
Soportes:        60°        (Ultra-mínimos)
Tiempo:          ~65%       (35% más rápido que Quality)
```
**Usar para**: Prototipos, verificar dimensiones, pruebas de ajuste

## 📏 EXPLICACIÓN TÉCNICA DE CADA AJUSTE

### **🏃‍♂️ VELOCIDADES - ¿Por qué estos valores?**

**Outer wall speed (35mm/s)**:
- **Propósito**: Calidad superficial y precisión dimensional
- **Física**: Velocidades altas causan vibraciones = líneas onduladas
- **Ender 2 Pro**: Frame ligero, necesita velocidades conservadoras
- **Aumentar si**: Superficie no importante (interior de piezas)
- **Reducir si**: Necesitas máxima precisión (engranajes, roscas)

**Inner wall speed (45mm/s)**:
- **Propósito**: Balance velocidad/calidad en paredes internas
- **Lógica**: No se ven, pueden ir más rápido que outer walls
- **Límite**: 45mm/s para evitar vibraciones en el frame
- **Aumentar si**: Pieza gruesa con muchas paredes internas
- **Reducir si**: Piezas con paredes muy delgadas

**Infill speed (60mm/s)**:
- **Propósito**: Eficiencia - el relleno no se ve
- **Límite físico**: Ender 2 Pro vibra mucho >70mm/s en infill
- **Beneficio**: Reduce tiempo total sin afectar calidad visible
- **Aumentar si**: Relleno muy denso (>20%) y frame bien calibrado
- **Reducir si**: Infill patterns complejos (gyroid, honeycomb)

**Travel speed (100mm/s)**:
- **Propósito**: Movimientos sin extruir - pueden ser rápidos
- **Límite**: Ender 2 Pro belt tension y rigidez del frame  
- **Riesgo**: >120mm/s causa belt slip y layer shift
- **Aumentar si**: Travel distances cortas y frame muy rígido
- **Reducir si**: Notas layer shifts o belt slipping

### **🌡️ TEMPERATURAS - ¿Por qué estos números?**

**Nozzle 205°C (PLA)**:
- **Viscosidad óptima**: Fluye bien sin babear
- **Adhesión intercapas**: Suficiente calor para fusión
- **Stringing**: 200-205°C minimiza hilos entre piezas
- **Aumentar si**: Subextrusión, velocidades muy altas, PLA+
- **Reducir si**: Muchos strings, oozing, detalles muy finos

**Bed 60°C primera capa / 55°C resto**:
- **Primera capa**: Máxima adhesión inicial
- **Resto**: Mantiene adhesión sin sobrecargar PSU
- **Warping**: Temperatura gradual reduce estrés térmico
- **Aumentar si**: Warping persistente, piezas muy grandes
- **Reducir si**: Overheating PSU, piezas muy pequeñas

### **🛠️ SOPORTES - Lógica detrás de cada valor**

**Support threshold 55°**:
- **Física**: PLA se auto-soporta hasta ~60° sin deformarse
- **Práctica**: 55° = balance seguro vs material desperdiciado
- **Tu error anterior**: 30° = soportes en lugares innecesarios
- **Aumentar si**: PLA de buena calidad, cooling excelente (hasta 65°)
- **Reducir si**: PLA barato, cooling deficiente, overhangs críticos

**Support XY distance 0.7mm**:
- **Adhesión controlada**: Suficiente soporte sin pegarse permanente
- **Remoción fácil**: Se despegan sin dañar superficie
- **Post-procesado**: Mínimo lijado necesario
- **Aumentar si**: Soportes muy pegados, superficie no crítica
- **Reducir si**: Overhangs muy críticos, superficie oculta

**Support interface 2 layers**:
- **Balance**: Suficiente soporte vs facilidad remoción
- **Calidad**: Base sólida para overhangs sin marks excesivos
- **Tiempo**: Compromiso entre calidad y velocidad
- **Aumentar si**: Overhangs muy críticos, calidad superficie importante
- **Reducir si**: Prototipo rápido, superficie no visible

### **📐 LAYER HEIGHT - ¿Cuándo cambiar?**

**0.2mm (Quality)**:
- **Propósito**: Balance perfecto resolución/tiempo
- **Detalles**: Capaz de imprimir texto de 2mm altura
- **Resistencia**: Adhesión intercapas óptima
- **Tiempo**: Base 100% para comparaciones

**0.3mm (Draft)**:
- **Propósito**: Velocidad máxima manteniendo calidad aceptable
- **Limitación**: Detalles <3mm se pierden
- **Beneficio**: 35% menos tiempo que 0.2mm
- **Resistencia**: Ligeramente menor por menos capas

**0.15mm (Fine)**:
- **Propósito**: Máxima calidad, detalles finos
- **Aplicación**: Miniaturas, joyería, logos pequeños
- **Costo**: +60% tiempo vs 0.2mm
- **Limitación**: Solo para piezas pequeñas en Ender 2 Pro

### **💨 REFRIGERACIÓN - Secuencia optimizada**

**0% primeras 3 capas**:
- **Warping**: Evita enfriamiento diferencial
- **Adhesión**: Permite que primera capa "se asiente"
- **Física**: PLA se contrae al enfriarse rápidamente

**25% capa 4, 75% capa 5+**:
- **Transición gradual**: Evita shock térmico
- **Overhangs**: Cooling progresivo para mejor calidad
- **Balance**: Suficiente para detalles, no tanto que cause warping

**100% bridges**:
- **Necesario**: Bridges necesitan enfriamiento inmediato
- **Física**: Filamento "vuela" sin soporte, debe solidificar rápido

## 📊 TIEMPOS ESTIMADOS COMPARATIVOS

| Tamaño modelo | Quality (0.2mm) | Draft (0.3mm) | Fine (0.15mm) |
|---------------|----------------|---------------|---------------|
| Pequeño (50x50mm) | 2-4h | 1.5-3h | 3-6h |
| Mediano (100x100mm) | 6-10h | 4-7h | 9-15h |
| Grande (150x150mm) | 12-20h | 8-14h | 18-30h |
| **Tu MacMini** | **~8.5h** | **~5.5h** | **~12h** |

## 🎯 CUÁNDO USAR CADA CONFIGURACIÓN

### **Quality_Ender2Pro** ✅
- Piezas finales/definitivas
- Modelos funcionales (tu MacMini)
- Cuando la superficie será visible
- Piezas que requieren resistencia
- Tolerancias dimensionales críticas

### **Draft_Ender2Pro** ⚡
- Prototipos y pruebas
- Verificar dimensiones/ajuste
- Modelos de concepto
- Piezas temporales
- Cuando el tiempo es crítico

### **Ajustes manuales ocasionales**:
- **Support threshold**: 45-65° según geometría específica
- **Infill density**: 10-25% según resistencia requerida  
- **Brim width**: 3-8mm según adhesión necesaria
- **Velocidades**: ±10mm/s según complejidad del modelo

## ⚠️ TROUBLESHOOTING RÁPIDO

**Warping/Esquinas levantadas:**
- ✅ Aumentar temperatura cama a 65°C
- ✅ Usar brim 8mm
- ✅ Verificar corrientes aire

**Soportes difíciles de quitar:**
- ✅ Aumentar XY distance a 0.8mm
- ✅ Reducir interface layers a 1
- ✅ Usar tree supports

**Mala calidad superficial:**
- ✅ Reducir velocidades 10mm/s
- ✅ Verificar tensión correas
- ✅ Lubricar ejes

**Subextrusión:**
- ✅ Aumentar temperatura 5°C
- ✅ Verificar E-steps calibration
- ✅ Limpiar nozzle

---
*Configuración optimizada basada en análisis técnico específico para Creality Ender 2 Pro*
*Actualizado: Septiembre 2025*