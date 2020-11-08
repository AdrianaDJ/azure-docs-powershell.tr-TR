---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274927"
---
# <span data-ttu-id="3788c-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3788c-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="3788c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3788c-102">SYNOPSIS</span></span>
<span data-ttu-id="3788c-103">Hizmet örneğinin meta verilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3788c-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="3788c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3788c-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3788c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3788c-105">DESCRIPTION</span></span>
<span data-ttu-id="3788c-106">Hizmet örneğinin meta verilerini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3788c-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="3788c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3788c-107">EXAMPLES</span></span>

### <span data-ttu-id="3788c-108">Örnek 1: cosmosdb teklif miktarı = 400 ile bir konum westus2 kaynak grubunda MyService adlı yeni bir Azure healthgelişme API 'leri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3788c-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

## <span data-ttu-id="3788c-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3788c-109">PARAMETERS</span></span>

### <span data-ttu-id="3788c-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="3788c-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="3788c-111">Access Ilkesi nesne kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="3788c-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="3788c-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="3788c-112">-AllowCorsCredential</span></span>
<span data-ttu-id="3788c-113">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="3788c-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="3788c-114">-AsJob</span></span>
<span data-ttu-id="3788c-115">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3788c-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="3788c-116">-Hedef kitle</span><span class="sxs-lookup"><span data-stu-id="3788c-116">-Audience</span></span>
<span data-ttu-id="3788c-117">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="3788c-118">Yetkili</span><span class="sxs-lookup"><span data-stu-id="3788c-118">-Authority</span></span>
<span data-ttu-id="3788c-119">Durumumerhır hizmet yetkilisi.</span><span class="sxs-lookup"><span data-stu-id="3788c-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="3788c-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="3788c-120">-CorsHeader</span></span>
<span data-ttu-id="3788c-121">Healthgelişme API 'leri CORS üstbilgisi için bir hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="3788c-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="3788c-122">İstek sırasında kullanılabilecek HTTP üst bilgilerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3788c-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="3788c-123">Herhangi bir üst bilgi için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="3788c-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="3788c-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="3788c-124">-CorsMaxAge</span></span>
<span data-ttu-id="3788c-125">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="3788c-126">Bir isteğin hangi süreyle saniye içinde önbelleğe alınacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3788c-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="3788c-127">Örnek: 600, 10 dakika anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3788c-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="3788c-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="3788c-128">-CorsMethod</span></span>
<span data-ttu-id="3788c-129">Healthgelişme API 'leri hizmet CORS yönteminin listesi.</span><span class="sxs-lookup"><span data-stu-id="3788c-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="3788c-130">-Corsorigın</span><span class="sxs-lookup"><span data-stu-id="3788c-130">-CorsOrigin</span></span>
<span data-ttu-id="3788c-131">Healthgelişme API 'leri, CORS başlangıç hizmet listesi.</span><span class="sxs-lookup"><span data-stu-id="3788c-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="3788c-132">Bu API 'ye erişebilen kaynak sitelerin URL 'Lerini belirtin veya herhangi bir siteden erişime izin vermek için \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="3788c-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="3788c-133">-Cosmosoffer,</span><span class="sxs-lookup"><span data-stu-id="3788c-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="3788c-134">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="3788c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3788c-135">-DefaultProfile</span></span>
<span data-ttu-id="3788c-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3788c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3788c-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="3788c-137">-EnableSmartProxy</span></span>
<span data-ttu-id="3788c-138">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="3788c-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3788c-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="3788c-140">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="3788c-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="3788c-141">-FhirVersion</span></span>
<span data-ttu-id="3788c-142">Fhır sürümü.</span><span class="sxs-lookup"><span data-stu-id="3788c-142">Fhir Version.</span></span>

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

### <span data-ttu-id="3788c-143">-Tür</span><span class="sxs-lookup"><span data-stu-id="3788c-143">-Kind</span></span>
<span data-ttu-id="3788c-144">Healthumerapı hizmeti türü.</span><span class="sxs-lookup"><span data-stu-id="3788c-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="3788c-145">Varsayılan değer Fhır</span><span class="sxs-lookup"><span data-stu-id="3788c-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="3788c-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="3788c-146">-Location</span></span>
<span data-ttu-id="3788c-147">Healthgelişme API 'leri hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="3788c-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="3788c-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3788c-148">-ManagedIdentity</span></span>
<span data-ttu-id="3788c-149">Yönetilen kimlik mi kullanıyorsunuz?</span><span class="sxs-lookup"><span data-stu-id="3788c-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="3788c-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="3788c-150">-Name</span></span>
<span data-ttu-id="3788c-151">Healthgelişme API 'leri hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="3788c-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="3788c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3788c-152">-ResourceGroupName</span></span>
<span data-ttu-id="3788c-153">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3788c-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="3788c-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3788c-154">-Tag</span></span>
<span data-ttu-id="3788c-155">Healthgelişme API 'leri</span><span class="sxs-lookup"><span data-stu-id="3788c-155">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="3788c-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="3788c-156">-Confirm</span></span>
<span data-ttu-id="3788c-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3788c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3788c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3788c-158">-WhatIf</span></span>
<span data-ttu-id="3788c-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3788c-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3788c-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3788c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3788c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3788c-161">CommonParameters</span></span>
<span data-ttu-id="3788c-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3788c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3788c-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3788c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3788c-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3788c-164">INPUTS</span></span>

### <span data-ttu-id="3788c-165">System. String</span><span class="sxs-lookup"><span data-stu-id="3788c-165">System.String</span></span>

## <span data-ttu-id="3788c-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3788c-166">OUTPUTS</span></span>

### <span data-ttu-id="3788c-167">Microsoft. Azure. Commands. Healthgelişme Apisservice. modeller. Pshealthumumısservice</span><span class="sxs-lookup"><span data-stu-id="3788c-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3788c-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3788c-168">NOTES</span></span>

## <span data-ttu-id="3788c-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3788c-169">RELATED LINKS</span></span>
