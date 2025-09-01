// JavaScript Example: Reading Entities
// Filterable fields: 
async function fetchEntityNameEntities() {
    const response = await fetch(`https://app.base44.com/api/apps/68b52b3a477b7c5636d65a50/entities/EntityName`, {
        headers: {
            'api_key': 'fc753b14154f471aa811874229663281', // or use await User.me() to get the API key
            'Content-Type': 'application/json'
        }
    });
    const data = await response.json();
    console.log(data);
}

// JavaScript Example: Updating an Entity
// Filterable fields: 
async function updateEntityNameEntity(entityId, updateData) {
    const response = await fetch(`https://app.base44.com/api/apps/68b52b3a477b7c5636d65a50/entities/EntityName/${entityId}`, {
        method: 'PUT',
        headers: {
            'api_key': 'fc753b14154f471aa811874229663281', // or use await User.me() to get the API key
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(updateData)
    });
    const data = await response.json();
    console.log(data);
}
