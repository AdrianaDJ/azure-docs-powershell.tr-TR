---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097420"
---
# <span data-ttu-id="0b1ca-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0b1ca-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="0b1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1ca-103">Önbelleğin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="0b1ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b1ca-104">SYNTAX</span></span>

### <span data-ttu-id="0b1ca-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b1ca-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1ca-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0b1ca-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b1ca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b1ca-107">DESCRIPTION</span></span>
<span data-ttu-id="0b1ca-108">API Yönetim hizmetinde yapılandırılmış önbelleğin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="0b1ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b1ca-109">EXAMPLES</span></span>

### <span data-ttu-id="0b1ca-110">Örnek 1: tüm önbellekleri alma</span><span class="sxs-lookup"><span data-stu-id="0b1ca-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="0b1ca-111">API Yönetim hizmetinde yapılandırılmış tüm önbelleklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="0b1ca-112">Örnek 2: tanımlayıcı westus tarafından belirtilen önbelleği alma</span><span class="sxs-lookup"><span data-stu-id="0b1ca-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="0b1ca-113">Westus için yapılandırılmış belirtilen önbelleğin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="0b1ca-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="0b1ca-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b1ca-114">PARAMETERS</span></span>

### <span data-ttu-id="0b1ca-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="0b1ca-115">-CacheId</span></span>
<span data-ttu-id="0b1ca-116">Bir önbelleğin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-116">Identifier of a cache.</span></span>
<span data-ttu-id="0b1ca-117">Belirtilmişse tanımlayıcının önbelleğini bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="0b1ca-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1ca-119">-Context</span><span class="sxs-lookup"><span data-stu-id="0b1ca-119">-Context</span></span>
<span data-ttu-id="0b1ca-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0b1ca-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1ca-122">-DefaultProfile</span></span>
<span data-ttu-id="0b1ca-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1ca-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b1ca-124">-ResourceId</span></span>
<span data-ttu-id="0b1ca-125">Bir önbelleğin ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="0b1ca-126">Belirtilmişse tanımlayıcının önbelleğini bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="0b1ca-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-127">This parameter is required.</span></span>

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

### <span data-ttu-id="0b1ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1ca-128">CommonParameters</span></span>
<span data-ttu-id="0b1ca-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1ca-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b1ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1ca-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b1ca-131">INPUTS</span></span>

### <span data-ttu-id="0b1ca-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="0b1ca-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b1ca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0b1ca-133">System.String</span></span>

## <span data-ttu-id="0b1ca-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b1ca-134">OUTPUTS</span></span>

### <span data-ttu-id="0b1ca-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="0b1ca-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="0b1ca-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b1ca-136">NOTES</span></span>

## <span data-ttu-id="0b1ca-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b1ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b1ca-138">Get-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="0b1ca-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="0b1ca-139">Set-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="0b1ca-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="0b1ca-140">Remove-Azapsananagementcache</span><span class="sxs-lookup"><span data-stu-id="0b1ca-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)