# Hajj Operations Management System
The Pilgrim's Journey: From Arrival to Departure

---

## 1. System Flowchart (مخطط انسياب العمليات)

```mermaid
graph TD
    A[Data Integration with Nusuk API] --> B[Virtual Allocation: Hotels & Camps]
    B --> C[Arrival at Port: Scan QR Code]
    C --> D[Transport to Hotel Makkah/Madinah]
    D --> E[Hotel Check-in & Catering Activation]
    E --> F[Mashaer Operations: Mina & Arafat]
    F --> G[Tafweej: Jamarat & Tawaf]
    G --> H[Departure Logistics & Return Transport]
    H --> I([Status: Departed])

    style A fill:#6d8e6c,stroke:#333,stroke-width:2px,color:#fff
    style F fill:#86a185,stroke:#333,stroke-width:2px,color:#fff
    style I fill:#f9f9f9,stroke:#333,stroke-width:2px,color:#000
