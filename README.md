# Fundamentos-Redes

# 📡 Redes: Router vs Switch vs Hub

## 1. Definiciones Simples

| Dispositivo | Definición "Para Humanos" | Capa OSI | Identificador |
|------------|--------------------------|----------|--------------|
| **Router** | El Director de Tráfico. Conecta redes distintas (Tu casa ↔ Internet). | Capa 3 (Red) | IP |
| **Switch** | El Organizador Interno. Conecta equipos en la misma red. | Capa 2 (Enlace) | MAC |
| **Hub** | El Repetidor Tonto. Copia todo a todos. (Obsoleto). | Capa 1 (Física) | Ninguno |

---

## 2. ¿Cómo funcionan realmente?

### 🔹 Router
- Mantiene una **Tabla de Rutas**.  
- Cuando llega un paquete, revisa la **IP de destino**.  
- Decide:  
  > "Esto no es de aquí, mándalo por la puerta correcta".  
- Evita que los datos se pierdan en Internet.

### 🔹 Switch
- Mantiene una **Tabla MAC**.  
- Aprende en qué puerto está cada dispositivo.  
- Envía datos **directamente al destino** (eficiente y rápido).  

### 🔹 Hub
- No tiene inteligencia.  
- Recibe datos y los envía a **todos los puertos**.  
- Genera colisiones y lentitud.  
- ❌ No se usa en redes modernas.

---

## 3. Conexión con Desarrollo (The Dev Side)

### 🌐 Router (IPs)
- Cuando haces:
  ```js
  fetch('https://api.tuapp.com')
