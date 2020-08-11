This template is launched from Panorama using Azure Orchestration Plugin which manages the firewall deployments. The plugin should be configured with a Service Principal with the following custom role permissions -

{
    "Name": "Panorama Azure Orchestration Role",
    "IsCustom": true,
    "Description": "Manage template deployments.",
    "Actions": [
        "Microsoft.Resources/subscriptions/resourcegroups/*",  
        "Microsoft.Resources/deployments/*",  
        "Microsoft.Network/networkSecurityGroups/*",  
        "Microsoft.Network/virtualNetworks/*",  
        "Microsoft.Insights/components/*",  
        "Microsoft.Network/loadBalancers/*",  
        "Microsoft.Compute/virtualMachineScaleSets/*",  
        "Microsoft.Insights/autoscalesettings/*",  
        "Microsoft.Network/routeTables/*",  
        "Microsoft.Network/publicIPAddresses/*",  
        "Microsoft.Network/applicationGateways/*",  
        "Microsoft.Compute/availabilitySets/*",  
        "Microsoft.Insights/metrics/*",  
        "Microsoft.Network/natGateways/*",  
        "Microsoft.Insights/metrics/*",  
        "Microsoft.Compute/virtualMachines/read",  
        "Microsoft.Network/networkInterfaces/read",  
        "Microsoft.Network/publicIPPrefixes/*"  
    ],  
    "NotActions": [
    ],  
    "AssignableScopes": [
        "/subscriptions/<subscription-uuid>"
    ]
}
