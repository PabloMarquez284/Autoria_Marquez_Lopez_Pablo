# Reto de Refactorización - TechNova Cloud v2.0
## Líneas de código ahorradas
Gracias a esta refactorización del código (xsd y xml) hemos ahorrado aproximadamente unas 10-20 líneas de código al usar grupos de los diferentes elementos, como son cpu, ram, gpu y discos. Con ello se ha evitado repetir la definicion de estos elementos en cada servidor, agrupándolos en un solo grupo.

## Restricción de ID único
A través de la restricción para que el id sea único y no pueda repetise, si se intentan definir dos servidores con el mismo id, VS Code muestra un error de validación indicando que el valor no es único. Un ejemplo sería este: "cvc-identity-constraint.4.1: Duplicate unique value [srv-db-01] found for identity constraint "uniqueId" of element "catalogo_cloud".xml(DuplicateUnique)". Esto ocurre porque el XSD obliga a que cada servidor tenga un idenitficador único dentro del documento.
