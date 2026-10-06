---
title: "CVE (Vulnerabilidades y Exposiciones Comunes)"
category: "Gestión de vulnerabilidades"
author: "@LuzSerranoDiaz"
tags:
  - ciberseguridad
  - cve
  - vulnerabilidades
  - exposiciones
  - web
summary: "CVE es un sistema de identificadores públicos que permite nombrar y consultar vulnerabilidades de ciberseguridad de forma consistente."
---

# CVE (Vulnerabilidades y Exposiciones Comunes)

<div class="term-meta-box">
  <div class="term-meta-item">
    <span class="term-meta-label">Categoría</span>
    <span class="term-meta-value">Gestión de vulnerabilidades</span>
  </div>
  <div class="term-meta-item">
    <span class="term-meta-label">Autor / Colaborador</span>
    <span class="term-meta-value"><a href="https://github.com/LuzSerranoDiaz" target="_blank">@LuzSerranoDiaz</a></span>
  </div>
</div>

## 📖 Definición
CVE (Common Vulnerabilities and Exposures, o Vulnerabilidades y Exposiciones Comunes) es un programa y catálogo de referencia que asigna identificadores únicos a vulnerabilidades de ciberseguridad divulgadas públicamente. Su objetivo es que fabricantes, investigadores, equipos de seguridad y herramientas puedan referirse al mismo problema sin confundirlo con otros ni depender de nombres distintos.

Un identificador CVE tiene el formato `CVE-AAAA-NNNN...`: incluye el año asociado al registro y un número de secuencia de longitud variable. Por ejemplo, `CVE-2021-44228` identifica la vulnerabilidad conocida como Log4Shell.

!!! note "Nota Importante"
  Un CVE identifica una vulnerabilidad; no indica por sí solo su gravedad, si un sistema concreto está afectado ni si se ha explotado. Para evaluar esos aspectos hay que consultar los detalles técnicos, las versiones afectadas y fuentes de enriquecimiento como NVD o CISA.

---

## ⚙️ Principios fundamentales

1. **Identificación única**: Cada registro aceptado recibe un identificador CVE estable, que puede usarse en avisos, inventarios, informes y herramientas de gestión de vulnerabilidades.
2. **Asignación coordinada**: Las CVE Numbering Authorities (CNA), como fabricantes y organizaciones autorizadas, pueden asignar identificadores y publicar información sobre vulnerabilidades dentro de su ámbito. El programa CVE coordina el sistema y mantiene el catálogo.
3. **Intercambio de información**: Los registros suelen incluir una descripción y referencias. Otras fuentes, como NVD, pueden añadir datos como puntuaciones CVSS y productos afectados; esa información complementaria no forma parte del identificador en sí.
4. **Evaluación contextual**: Las organizaciones deben contrastar el CVE con los productos y versiones que usan, la disponibilidad de parches y la exposición real de sus sistemas para priorizar la respuesta.

---

## 🎯 Ejemplo práctico: Log4Shell

`CVE-2021-44228` es el identificador de Log4Shell, una vulnerabilidad de ejecución remota de código en Apache Log4j 2. Una organización puede usarlo para localizar el aviso oficial, determinar si sus aplicaciones incluyen una versión afectada y coordinar la actualización.

Un flujo de respuesta simplificado sería:

1. Buscar `CVE-2021-44228` en CVE.org y revisar la descripción y las referencias del registro.
2. Comparar las versiones de Log4j detectadas en el inventario con las versiones afectadas y las correcciones indicadas por Apache.
3. Actualizar los componentes vulnerables a una versión corregida y verificar que la actualización se haya aplicado en todos los servicios pertinentes.
4. Consultar fuentes como NVD y CISA KEV para enriquecer la priorización, sin asumir que la presencia del identificador demuestra por sí misma que un sistema es vulnerable o fue comprometido.

El ejemplo muestra el uso del CVE como referencia compartida durante la identificación y remediación; no es una prueba de explotación ni una medida de severidad.

---

## 🛡️ Buenas prácticas

- Mantener un inventario actualizado de productos, dependencias y versiones para identificar qué activos podrían estar afectados.
- Validar los datos del CVE con avisos del fabricante y fuentes reconocidas; no priorizar únicamente por el año o número del identificador.
- Aplicar parches o mitigaciones recomendadas, y documentar la verificación y el riesgo residual.

---

## 🔗 Referencias y Enlaces de Interés
- [Programa y catálogo CVE](https://www.cve.org/)
- [NVD: registro de CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228)
- [Aviso de seguridad de Apache Log4j](https://logging.apache.org/log4j/2.x/security.html)
- [CISA Known Exploited Vulnerabilities (KEV) Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
