# Capítulo IV: Strategic-Level Software Design

## 4.1. Strategic-Level Attribute-Driven Design

### 4.1.1. Design Purpose

### 4.1.2. Attribute-Driven Design Inputs

#### 4.1.2.1. Primary Functionality (Primary User Stories)

#### 4.1.2.2. Quality Attribute Scenarios

#### 4.1.2.3. Constraints

### 4.1.3. Architectural Drivers Backlog

### 4.1.4. Architectural Design Decisions

### 4.1.5. Quality Attribute Scenario Refinements

## 4.2. Strategic-Level Domain-Driven Design

### 4.2.1. EventStorming

### 4.2.2. Candidate Context Discovery

### 4.2.3. Domain Message Flows Modeling
En esta sección se explica y evidencia el proceso seguido para visualizar cómo deben colaborar los bounded contexts al resolver los casos que se presentan en el negocio para las personas usuarias del sistema. Para ello se aplicó la técnica de visualización Domain Storytelling.

Cada historia se construyó a partir del comportamiento realmente implementado en el backend (intiva-api-platform): los command y query handlers, los domain events publicados y los servicios de Anti-Corruption Layer (ACL) que consume cada contexto. En lugar de la notación icónica clásica, las historias se representan como diagramas de secuencia por carriles —uno por actor o bounded context—, donde cada flecha numerada corresponde a una oración de la historia (actor — actividad — objeto de trabajo — destinatario), preservando el orden narrativo que exige Domain Storytelling.

Se seleccionaron cinco historias que cubren los procesos de negocio más representativos: el alta de una persona usuaria, la formación de una economía familiar, el registro de una transacción con evaluación de límite de gasto, el recordatorio de un pago recurrente y la consulta del panel de analíticas.
#### 4.2.3.1. Historia 1 — Registro y preparación inicial de una nueva persona usuaria

#### 4.2.3.2. Historia 2 — Una economía familiar se organiza (Household)

#### 4.2.3.3. Historia 3 — Se registra una transacción familiar y se evalúa un límite de gasto

#### 4.2.3.4. Historia 4 — Un pago recurrente está por vencer

#### 4.2.3.5. Historia 5 — La familia visualiza sus métricas financieras

### 4.2.4. Bounded Context Canvases

#### 4.2.4.1. Identity and Access Management (IAM)

#### 4.2.4.2. Profiles

#### 4.2.4.3. Categories & Financial Accounts

#### 4.2.4.4. Finances

#### 4.2.4.5. Financial Goals (Savings)

#### 4.2.4.6. Household

#### 4.2.4.7. Communications

#### 4.2.4.8. Analytics

### 4.2.5. Context Mapping

#### Tabla de relaciones entre bounded contexts

#### Shared Kernel

#### Discusión de diseño: preguntas "¿qué pasaría si…?"

## 4.3. Software Architecture

### 4.3.1. Software Architecture System Landscape Diagram

### 4.3.2. Software Architecture Context Level Diagrams

### 4.3.3. Software Architecture Container Level Diagrams

### 4.3.4. Software Architecture Deployment Diagrams