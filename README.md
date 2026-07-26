📄 Project & ERD Description
Project Title
Digital Transformation for Maritime Navigation & Port Rerouting: A Database Model for Strait of Hormuz Contingency Management

Overview & Vision (Alignment with Oman Vision 2040)
This ER diagram represents a centralized relational data model designed to support Oman’s Vision 2040 digital transformation strategy in the maritime and logistics sector.

In the event of a critical closure or restriction at the Strait of Hormuz, vessels bound for ports inside the Arabian Gulf face severe congestion and operational delays at sea. This database system links all major Omani ports into a unified data network to enable dynamic, automated, and accurate rerouting of ships. By digitally orchestrating trip statuses, vessel specifications, port capacities, and weather conditions, the system minimizes sea anchoring, optimizes cargo offloading, and speeds up emergency decision-making.

Entity & Architectural Details
SHIP Entity:

Purpose: Stores core vessel identification and real-time positioning metrics.

Key Attributes: IMO Number (Primary Key), MMSI, VesselName, and VesselType.

Tracking Attributes: Captures live navigation parameters including latitude, longitude, speed over ground, course direction, Position, Movement, and vessel Status.

Port Entity:

Purpose: Represents Omani and regional ports integrated into the centralized network.

Key Attributes: Port Name (Primary Key), Country, Port Location Type (e.g., Outside Strait vs. Inside Gulf), and capacity dimensions (Operational Capacity & Handling Capacity).

Strategic Role: Enables real-time assessment of Omani ports outside the Strait of Hormuz to evaluate their readiness for receiving diverted vessels.

Trip Entity & Diversion Logic:

Purpose: Tracks vessel journeys, original destinations, and emergency rerouting events.

Relationships:

Bound_To: Connects a Trip to its original intended destination Port.

Diverted_To: Connects a Trip to an alternative Omani Port when rerouting occurs.

Tracking Attributes: Captures travel metrics (DISTANCE), trip states (Status), and the specific cause for rerouting (Diversion_Reason).

Weather Entity:

Purpose: Monitors environmental and sea conditions associated with target ports.

Relationship: Connected via HAS to Port to ensure safe docking, offloading, and maritime risk assessment during emergency diversions.

Key Impact & Value Proposition
Digital Rerouting: Instantly identifies optimal alternative Omani ports outside the strait based on current port handling capacity and geographical location.

Congestion Prevention: Prevents vessel stacking and long wait times in international waters.

Enhanced Offloading Efficiency: Improves cargo reception accuracy and speeds up port operations through centralized data availability.
