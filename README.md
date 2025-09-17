# SUC-FI-02.05 – Congestion Management Planning

## General Information and Purpose

**Service Name/Title:** Congestion Management Planning  
**Description and Purpose:** Short-term congestion management planning based on forecasted congestion cases and available flexibility.  
**Owner/Contact Information:** TAU  

---

## Functional Requirements

- Receive data on congestion forecast (SUC-FI-02.01).  
- Use grid model data.  
- Use data on distributed energy resources (DERs).  
- Validate incoming data, checking for anomalies and outliers.  
- Harmonise the input data for processing.  
- Run algorithms to identify remedies for forecasted congestion cases.  
- Publish congestion management planning results to the message broker.  
- Receive necessary data from the message broker.  

---

## Non-Functional Requirements

- Congestion forecast data should be available for processing.  
- Incoming data should always be valid.  
- **99.9% uptime** for the service.  

---

## Service Interfaces

- **Visualization:** Grafana (or equivalent) will be used to visualize forecasts and congestion management results.  
- **API Integration:** Grafana uses a premade HTTP API; no additional service interfaces are required for this implementation.  

---

## Data Model

- **Entities and Relationships:** To be defined, expected to include congestion forecasts, DER availability, and grid model data.  
- **Database Schema:** To be aligned with grid state forecasting and congestion forecasting models.  

---

## Integration and Dependencies

- **External Dependencies:** Congestion Forecasting Service (SUC-FI-02.01).  
- **System Dependencies:** Grid topology and DER data sources.  
- **Third-party Integrations:** Grafana for visualization.  
- **HEDGE-IoT Edge Devices & Cloud Services:** Integration for DER and flexibility input.  
- **Integration with App Store:** To be defined.  
- **Integration with Data Space:** To be defined.  

---

## Security and Privacy

- **Data Sensitivity:** Handles grid congestion forecasts, grid model data, and DER information (critical infrastructure).  
- **Access Control:** Role-based access and service-level authorization.  
- **Audit Logs:** System must keep track of received data, algorithm execution, and published results.  

---

## Performance Considerations

- **Stress Testing:** Required to ensure robustness under high volumes of DER and congestion forecast data.  
- **Response Times:** Results must be generated in time to support short-term congestion management planning.  

---

## Deployment and Environment

- **Configuration:** Aligned with other Finnish pilot forecasting services.  
- **CI/CD:** Automated deployment pipelines for updates and bug fixes.  
- **Monitoring and Logging:** Continuous monitoring of service uptime, performance, and anomalies.  

---

## Testing and Validation

- **Test Cases:** Validation of input harmonization, congestion forecast usage, and DER flexibility allocation.  
- **Automated Testing Tools:** For regression and integration testing.  
- **Acceptance Tests:** End-to-end validation of congestion management planning workflows.  
