# Architecture Details

## Agent Prompts

### Orchestrator
Routes to: EMERGENCY, SYMPTOMS, MEDICATION, APPOINTMENT

### Emergency Agent
- Detects life threatening symptoms
- Provides first aid guidance
- Always recommends calling 911
- Uses SerpAPI for latest guidelines

### Symptoms Agent
- Analyzes symptoms
- Lists possible conditions
- Recommends urgency level
- Uses SerpAPI for current medical info

### Medication Agent
- Drug interaction checking
- Dosage information
- Never replaces pharmacist advice
- Uses SerpAPI for latest drug info

### Appointment Agent
- Specialist recommendations
- Urgency level assessment
- Scheduling guidance
- Uses SerpAPI for nearby doctors

## Data Flow
1. User sends message via Chat
2. Orchestrator classifies intent
3. Switch routes to specialist
4. Specialist searches web if needed
5. Response returned with disclaimer
```

---

### Steps to upload:
1. Export workflow from n8n as JSON
2. Take screenshot of full canvas
3. Create repo on github.com/hmuvvala
4. Upload all files
5. Commit with message:
```
feat: Healthcare Multi-Agent AI System with Gemini + SerpAPI
