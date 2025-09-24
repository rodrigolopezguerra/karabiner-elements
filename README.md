# karabiner-elements
Karabiner Elements español para teclado ABC de mac


# Configuración personalizada de Karabiner-Elements

Este archivo de configuración permite escribir caracteres acentuados y la letra `ñ` usando la tecla `[` como tecla modificadora especial. También redefine combinaciones para insertar corchetes y llaves de forma rápida.  

---

## 📌 Descripción general

- `[ + vocal` → genera **vocal con tilde** (`á, é, í, ó, ú`)  
- `[ + n` → genera **ñ**  
- `[ + espacio` → genera `[`  
- `[ + shift + espacio` → genera `{`  

El sistema funciona activando una **variable temporal (`accent_bracket`)** al presionar `[`. Mientras esta variable esté activa, la siguiente tecla se transforma según las reglas.

---

## 🔤 Reglas principales

1. **Vocales minúsculas con acento**  
   - `[ + a` → á  
   - `[ + e` → é  
   - `[ + i` → í  
   - `[ + o` → ó  
   - `[ + u` → ú  

2. **Vocales mayúsculas con acento**  
   - `[ + Shift + A` → Á  
   - `[ + Shift + E` → É  
   - `[ + Shift + I` → Í  
   - `[ + Shift + O` → Ó  
   - `[ + Shift + U` → Ú  

3. **Letra ñ**  
   - `[ + n` → ñ  
   - `[ + Shift + N` → Ñ  

4. **Corchetes y llaves**  
   - `[ + espacio` → `[`  
   - `[ + Shift + espacio` → `{`  

5. **Cualquier otra tecla**  
   - Si presionas `[ + (consonante o número)` se imprime directamente `[` seguido de la tecla correspondiente.  
     - Ejemplo: `[ + b` → `[b`  
     - Ejemplo: `[ + 3` → `[3`

---

## ⚙️ Funcionamiento interno

- **`accent_bracket`** se activa al presionar `[`.  
- La siguiente tecla es interceptada y transformada según la regla definida.  
- Luego la variable se resetea automáticamente a `0` para que el sistema vuelva al estado normal.  

Esto asegura que el modificador solo afecta a **una tecla a la vez**, imitando un "modo acento" temporal.

---

## 🚀 Instalación

1. Abre **Karabiner-Elements** en tu Mac.  
2. Ve a la pestaña **Complex Modifications**.  
3. Haz clic en **Add Rule**.  
4. Importa este archivo JSON o copia su contenido en:  ~/.config/karabiner/assets/complex_modifications/
5. Activa la regla desde la interfaz de Karabiner.  

---

## ✅ Ejemplos de uso

- Escribir `árbol`: `[ + a` → á → escribes "rbol" → **árbol**  
- Escribir `Ñu`: `[ + Shift + N` → Ñ → escribes "u" → **Ñu**  
- Escribir `{hola}`: `[ + Shift + espacio` → `{` → escribes "hola" → `[ + Shift + espacio` → `}`  

---

## 📝 Notas

- Este sistema está pensado para **escribir en español** con teclado en inglés sin necesidad de cambiar de layout.  
- Las reglas cubren letras con tilde, ñ, corchetes y llaves.  
- Si presionas una tecla no definida (ejemplo `[ + k`), se imprime `[k`.  

---
