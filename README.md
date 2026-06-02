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
```
erDiagram
    PILGRIM {
        string pilgrim_id
        string name
        string nationality
        string boundary_no
        string status
    }
    GROUP {
        string group_id
        string supervisor_name
        string nationality
        int total_pilgrims
    }
    ACCOMMODATION {
        string accommodation_id
        string type_Hotel_or_Camp
        string city_or_Mashaer
        int capacity
        string gps_location
    }
    TRANSPORT {
        string transport_id
        string plate_no
        string driver_name
        string driver_phone
        string route
    }
    CATERING {
        string catering_id
        string meal_type
        string delivery_time
        string contractor_name
        string status
    }

    GROUP ||--|{ PILGRIM : "contains"
    PILGRIM }|--|| ACCOMMODATION : "stays_at"
    GROUP }|--|| TRANSPORT : "uses"
    ACCOMMODATION ||--|{ CATERING : "receives"
