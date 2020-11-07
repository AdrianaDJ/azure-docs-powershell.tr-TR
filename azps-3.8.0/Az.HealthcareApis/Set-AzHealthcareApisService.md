---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 070ff5ee85687662d11cb30e3e3e7370b29ac251
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937357"
---
# <span data-ttu-id="dc989-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="dc989-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="dc989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc989-102">SYNOPSIS</span></span>
<span data-ttu-id="dc989-103">Var olan bir Healthsır API 'si hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc989-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="dc989-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc989-104">SYNTAX</span></span>

### <span data-ttu-id="dc989-105">ServiceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc989-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc989-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dc989-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc989-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="dc989-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc989-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc989-108">DESCRIPTION</span></span>
<span data-ttu-id="dc989-109">Var olan bir Healthsır API 'si hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc989-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="dc989-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc989-110">EXAMPLES</span></span>

### <span data-ttu-id="dc989-111">Örnek 1: cosmosdb Offerüretiminin = 500 ile kaynak grubundaki MyService adındaki mevcut healthgelişme API 'lerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc989-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

### <span data-ttu-id="dc989-112">Örnek 2: cosmosdb Offerüretiminin = 500 ile kaynak grubundaki MyService adındaki mevcut healthgelişme API 'lerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc989-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

## <span data-ttu-id="dc989-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc989-113">PARAMETERS</span></span>

### <span data-ttu-id="dc989-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="dc989-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="dc989-115">Access Ilkesi nesne kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="dc989-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="dc989-116">-AllowCorsCredential</span></span>
<span data-ttu-id="dc989-117">Healthgelişme API 'leri fhir</span><span class="sxs-lookup"><span data-stu-id="dc989-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="dc989-118">-AsJob</span></span>
<span data-ttu-id="dc989-119">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dc989-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-120">-Hedef kitle</span><span class="sxs-lookup"><span data-stu-id="dc989-120">-Audience</span></span>
<span data-ttu-id="dc989-121">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-122">Yetkili</span><span class="sxs-lookup"><span data-stu-id="dc989-122">-Authority</span></span>
<span data-ttu-id="dc989-123">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="dc989-124">-CorsHeader</span></span>
<span data-ttu-id="dc989-125">Healthgelişme API 'leri CORS üstbilgisi için bir hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="dc989-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="dc989-126">İstek sırasında kullanılabilecek HTTP üst bilgilerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="dc989-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="dc989-127">Herhangi bir üst bilgi için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc989-127">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="dc989-128">-CorsMaxAge</span></span>
<span data-ttu-id="dc989-129">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="dc989-130">Bir isteğin hangi süreyle saniye içinde önbelleğe alınacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dc989-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="dc989-131">Örnek: 600, 10 dakika anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="dc989-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="dc989-132">-CorsMethod</span></span>
<span data-ttu-id="dc989-133">Healthgelişme API 'leri, CORS yöntemlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="dc989-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-134">-Corsorigın</span><span class="sxs-lookup"><span data-stu-id="dc989-134">-CorsOrigin</span></span>
<span data-ttu-id="dc989-135">Healthgelişme API 'leri CORS kaynakları listesi.</span><span class="sxs-lookup"><span data-stu-id="dc989-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="dc989-136">Healthgelişme API 'leri, CORS başlangıç hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="dc989-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="dc989-137">Bu API 'ye erişebilen kaynak sitelerin URL 'Lerini belirtin veya herhangi bir siteden erişime izin vermek için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc989-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-138">-Cosmosoffer,</span><span class="sxs-lookup"><span data-stu-id="dc989-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="dc989-139">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc989-140">-DefaultProfile</span></span>
<span data-ttu-id="dc989-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc989-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc989-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="dc989-142">-DisableCorsCredential</span></span>
<span data-ttu-id="dc989-143">Healthgelişme API 'lerini FhirService CorsCredentials Izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="dc989-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="dc989-144">-DisableSmartProxy</span></span>
<span data-ttu-id="dc989-145">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="dc989-146">-EnableSmartProxy</span></span>
<span data-ttu-id="dc989-147">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc989-148">-InputObject</span></span>
<span data-ttu-id="dc989-149">Healthgelişme API 'Leri Get-Azhealthumalısfhirpget 'den yöneltilen fhır hizmeti.</span><span class="sxs-lookup"><span data-stu-id="dc989-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc989-150">-Name</span></span>
<span data-ttu-id="dc989-151">Healthgelişme API 'leri hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="dc989-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="dc989-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc989-152">-ResourceGroupName</span></span>
<span data-ttu-id="dc989-153">Healthumerapı hizmet kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dc989-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="dc989-154">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dc989-154">-ResourceId</span></span>
<span data-ttu-id="dc989-155">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="dc989-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dc989-156">-Tag</span></span>
<span data-ttu-id="dc989-157">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="dc989-157">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc989-158">-Confirm</span></span>
<span data-ttu-id="dc989-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc989-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc989-160">-WhatIf</span></span>
<span data-ttu-id="dc989-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc989-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc989-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc989-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc989-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc989-163">CommonParameters</span></span>
<span data-ttu-id="dc989-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc989-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc989-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc989-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc989-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc989-166">INPUTS</span></span>

### <span data-ttu-id="dc989-167">System. String</span><span class="sxs-lookup"><span data-stu-id="dc989-167">System.String</span></span>

### <span data-ttu-id="dc989-168">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="dc989-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="dc989-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc989-169">OUTPUTS</span></span>

### <span data-ttu-id="dc989-170">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="dc989-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="dc989-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc989-171">NOTES</span></span>

## <span data-ttu-id="dc989-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc989-172">RELATED LINKS</span></span>
