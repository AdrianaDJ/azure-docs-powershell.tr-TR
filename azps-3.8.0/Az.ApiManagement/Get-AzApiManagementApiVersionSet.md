---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 2b87f3b0716c95f27a78c2a0f59168f133ade015
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097425"
---
# <span data-ttu-id="711ad-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="711ad-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="711ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="711ad-102">SYNOPSIS</span></span>
<span data-ttu-id="711ad-103">API sürüm kümelerinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="711ad-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="711ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="711ad-104">SYNTAX</span></span>

### <span data-ttu-id="711ad-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="711ad-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711ad-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="711ad-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="711ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="711ad-107">DESCRIPTION</span></span>
<span data-ttu-id="711ad-108">**Get-Azapsananagementapıversionset** cmdlet 'ı, API yönetim BAĞLAMıNDA yapılandırılmış API sürüm kümelerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="711ad-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="711ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="711ad-109">EXAMPLES</span></span>

### <span data-ttu-id="711ad-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="711ad-110">Example 1</span></span>

### <span data-ttu-id="711ad-111">Örnek 1: tüm API sürüm kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="711ad-111">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="711ad-112">Bu komut, belirtilen bağlam için tüm API sürüm kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="711ad-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="711ad-113">Örnek 2: KIMLIĞE göre ayarlanan bir API sürümü alma</span><span class="sxs-lookup"><span data-stu-id="711ad-113">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="711ad-114">Bu komut belirtilen KIMLIĞE sahip API sürüm kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="711ad-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="711ad-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="711ad-115">PARAMETERS</span></span>

### <span data-ttu-id="711ad-116">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="711ad-116">-ApiVersionSetId</span></span>
<span data-ttu-id="711ad-117">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="711ad-117">API identifier to look for.</span></span>
<span data-ttu-id="711ad-118">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="711ad-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="711ad-119">-Context</span><span class="sxs-lookup"><span data-stu-id="711ad-119">-Context</span></span>
<span data-ttu-id="711ad-120">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="711ad-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="711ad-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="711ad-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711ad-122">-DefaultProfile</span></span>
<span data-ttu-id="711ad-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="711ad-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="711ad-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="711ad-124">-ResourceId</span></span>
<span data-ttu-id="711ad-125">Apıversionset 'in ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="711ad-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="711ad-126">Belirtilmişse tanımlayıcı tarafından Apıversionset bulmayı dener.</span><span class="sxs-lookup"><span data-stu-id="711ad-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="711ad-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="711ad-127">This parameter is required.</span></span>

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

### <span data-ttu-id="711ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ad-128">CommonParameters</span></span>
<span data-ttu-id="711ad-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="711ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ad-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="711ad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ad-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="711ad-131">INPUTS</span></span>

### <span data-ttu-id="711ad-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="711ad-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="711ad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="711ad-133">System.String</span></span>

## <span data-ttu-id="711ad-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="711ad-134">OUTPUTS</span></span>

### <span data-ttu-id="711ad-135">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="711ad-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="711ad-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="711ad-136">NOTES</span></span>

## <span data-ttu-id="711ad-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="711ad-137">RELATED LINKS</span></span>

[<span data-ttu-id="711ad-138">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="711ad-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="711ad-139">Remove-Azapsananagementapiset</span><span class="sxs-lookup"><span data-stu-id="711ad-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="711ad-140">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="711ad-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)