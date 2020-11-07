---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 0f5aff6cfe499d9d0ef37d299babb178b437c2e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751792"
---
# <span data-ttu-id="19243-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="19243-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="19243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19243-102">SYNOPSIS</span></span>
<span data-ttu-id="19243-103">Hizmet örneğinin meta verilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="19243-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="19243-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19243-104">SYNTAX</span></span>

### <span data-ttu-id="19243-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19243-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19243-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19243-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19243-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="19243-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19243-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="19243-108">DESCRIPTION</span></span>
<span data-ttu-id="19243-109">Belirtilen abonelikte veya bir kaynak grubunda oluşturulmuş mevcut Healthhır hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="19243-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="19243-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19243-110">EXAMPLES</span></span>

### <span data-ttu-id="19243-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19243-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="19243-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="19243-112">Example 2</span></span>

<span data-ttu-id="19243-113">Sağlanan kaynak grubundaki tüm Healthgelişme API hizmetleri için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="19243-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="19243-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="19243-114">Example 3</span></span>

<span data-ttu-id="19243-115">Verilen abonelikteki tüm Healthgelişme API hizmetleri için meta verileri alır</span><span class="sxs-lookup"><span data-stu-id="19243-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="19243-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19243-116">PARAMETERS</span></span>

### <span data-ttu-id="19243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19243-117">-DefaultProfile</span></span>
<span data-ttu-id="19243-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19243-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19243-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="19243-119">-Name</span></span>
<span data-ttu-id="19243-120">Healthgelişme API 'leri hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="19243-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19243-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19243-121">-ResourceGroupName</span></span>
<span data-ttu-id="19243-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="19243-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19243-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="19243-123">-ResourceId</span></span>
<span data-ttu-id="19243-124">Kaynak kimliği adı.</span><span class="sxs-lookup"><span data-stu-id="19243-124">Resource Id Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19243-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19243-125">CommonParameters</span></span>
<span data-ttu-id="19243-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19243-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19243-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19243-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19243-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19243-128">INPUTS</span></span>

### <span data-ttu-id="19243-129">System. String</span><span class="sxs-lookup"><span data-stu-id="19243-129">System.String</span></span>

## <span data-ttu-id="19243-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19243-130">OUTPUTS</span></span>

### <span data-ttu-id="19243-131">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="19243-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="19243-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19243-132">NOTES</span></span>

## <span data-ttu-id="19243-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19243-133">RELATED LINKS</span></span>
