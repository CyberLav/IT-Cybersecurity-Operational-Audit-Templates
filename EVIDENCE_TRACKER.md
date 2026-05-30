# Evidence Request Tracker

A standardized utility for tracking the lifecycle of audit artifacts. This tracker ensures that every piece of evidence—logs, configurations, screenshots, or interview data—is formally requested, received, and validated.

## 📋 Tracker Schema

Use the following structure for your Evidence Request Log:

| Field | Description |
| :--- | :--- |
| **Request ID** | Unique identifier (e.g., `REQ-001`). |
| **Audit Step** | Link to the specific control in the *Risk Control Matrix*. |
| **Description** | Detailed requirement for the artifact. |
| **Owner** | Primary client contact responsible for the data. |
| **Status** | Lifecycle state: `Pending`, `In-Progress`, `Received`, `Validated`. |
| **Date Requested** | Date the request was issued (for SLA tracking). |
| **Evidence Path** | URI/Link to the secure storage repository. |

## ⚙️ Progress Logic
Implement the following logic (or similar) in your tracking sheet to monitor engagement health:

```javascript
/**
 * Calculates percentage of completed evidence.
 * @param {Array} requests - The array of request objects.
 * @returns {string} - Completion percentage.
 */
function getProgress(requests) {
    const total = requests.length;
    if (total === 0) return "0%";
    
    const completed = requests.filter(r => 
        r.status === "Received" || r.status === "Validated"
    ).length;
    
    return `${Math.round((completed / total) * 100)}%`;
}
