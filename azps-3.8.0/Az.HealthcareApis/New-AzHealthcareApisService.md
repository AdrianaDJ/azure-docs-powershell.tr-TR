---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f4bc87424707fe3f26da04a4984b2ae122d98a3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937362"
---
# <span data-ttu-id="fe8c6-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="fe8c6-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="fe8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8c6-103">Hizmet örneğinin meta verilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="fe8c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe8c6-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe8c6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe8c6-106">Hizmet örneğinin meta verilerini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="fe8c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe8c6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe8c6-108">Örnek 1: cosmosdb teklif miktarı = 400 ile bir konum westus2 kaynak grubunda MyService adlı yeni bir Azure healthgelişme API 'leri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

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

## <span data-ttu-id="fe8c6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe8c6-109">PARAMETERS</span></span>

### <span data-ttu-id="fe8c6-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="fe8c6-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="fe8c6-111">Access Ilkesi nesne kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-111">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="fe8c6-112">-AllowCorsCredential</span></span>
<span data-ttu-id="fe8c6-113">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="fe8c6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="fe8c6-114">-AsJob</span></span>
<span data-ttu-id="fe8c6-115">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="fe8c6-116">-Hedef kitle</span><span class="sxs-lookup"><span data-stu-id="fe8c6-116">-Audience</span></span>
<span data-ttu-id="fe8c6-117">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-117">HealthcareApis Fhir Service Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-118">Yetkili</span><span class="sxs-lookup"><span data-stu-id="fe8c6-118">-Authority</span></span>
<span data-ttu-id="fe8c6-119">Durumumerhır hizmet yetkilisi.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-119">HealthcareApis Fhir Service Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="fe8c6-120">-CorsHeader</span></span>
<span data-ttu-id="fe8c6-121">Healthgelişme API 'leri CORS üstbilgisi için bir hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="fe8c6-122">İstek sırasında kullanılabilecek HTTP üst bilgilerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="fe8c6-123">Herhangi bir üst bilgi için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-123">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="fe8c6-124">-CorsMaxAge</span></span>
<span data-ttu-id="fe8c6-125">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="fe8c6-126">Bir isteğin hangi süreyle saniye içinde önbelleğe alınacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="fe8c6-127">Örnek: 600, 10 dakika anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-127">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="fe8c6-128">-CorsMethod</span></span>
<span data-ttu-id="fe8c6-129">Healthgelişme API 'leri hizmet CORS yönteminin listesi.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-130">-Corsorigın</span><span class="sxs-lookup"><span data-stu-id="fe8c6-130">-CorsOrigin</span></span>
<span data-ttu-id="fe8c6-131">Healthgelişme API 'leri, CORS başlangıç hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="fe8c6-132">Bu API 'ye erişebilen kaynak sitelerin URL 'Lerini belirtin veya herhangi bir siteden erişime izin vermek için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-133">-Cosmosoffer,</span><span class="sxs-lookup"><span data-stu-id="fe8c6-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="fe8c6-134">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8c6-135">-DefaultProfile</span></span>
<span data-ttu-id="fe8c6-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe8c6-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="fe8c6-137">-EnableSmartProxy</span></span>
<span data-ttu-id="fe8c6-138">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="fe8c6-139">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="fe8c6-139">-FhirVersion</span></span>
<span data-ttu-id="fe8c6-140">Fhır sürümü.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-140">Fhir Version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-141">-Tür</span><span class="sxs-lookup"><span data-stu-id="fe8c6-141">-Kind</span></span>
<span data-ttu-id="fe8c6-142">Healthumerapı hizmeti türü.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="fe8c6-143">Varsayılan değer Fhır</span><span class="sxs-lookup"><span data-stu-id="fe8c6-143">The default value is Fhir</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-144">-Konum</span><span class="sxs-lookup"><span data-stu-id="fe8c6-144">-Location</span></span>
<span data-ttu-id="fe8c6-145">Healthgelişme API 'leri hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-145">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe8c6-146">-Name</span></span>
<span data-ttu-id="fe8c6-147">Healthgelişme API 'leri hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-147">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8c6-148">-ResourceGroupName</span></span>
<span data-ttu-id="fe8c6-149">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-149">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fe8c6-150">-Tag</span></span>
<span data-ttu-id="fe8c6-151">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="fe8c6-151">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8c6-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe8c6-152">-Confirm</span></span>
<span data-ttu-id="fe8c6-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8c6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8c6-154">-WhatIf</span></span>
<span data-ttu-id="fe8c6-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8c6-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8c6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8c6-157">CommonParameters</span></span>
<span data-ttu-id="fe8c6-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8c6-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe8c6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8c6-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe8c6-160">INPUTS</span></span>

### <span data-ttu-id="fe8c6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="fe8c6-161">System.String</span></span>

## <span data-ttu-id="fe8c6-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe8c6-162">OUTPUTS</span></span>

### <span data-ttu-id="fe8c6-163">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="fe8c6-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="fe8c6-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe8c6-164">NOTES</span></span>

## <span data-ttu-id="fe8c6-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe8c6-165">RELATED LINKS</span></span>
