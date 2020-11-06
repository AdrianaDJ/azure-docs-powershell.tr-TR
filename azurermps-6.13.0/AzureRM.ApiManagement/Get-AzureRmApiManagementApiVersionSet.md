---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591476"
---
# <span data-ttu-id="d1cd5-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d1cd5-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d1cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cd5-103">API sürüm kümelerinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="d1cd5-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1cd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1cd5-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1cd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="d1cd5-106">**Get-Azurermapsananagementapiversionset** cmdlet 'i, bir API yönetim BAĞLAMıNDA yapılandırılmış API sürüm kümelerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="d1cd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="d1cd5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1cd5-108">Example 1</span></span>

### <span data-ttu-id="d1cd5-109">Örnek 1: tüm API sürüm kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="d1cd5-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="d1cd5-110">Bu komut, belirtilen bağlam için tüm API sürüm kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="d1cd5-111">Örnek 2: KIMLIĞE göre ayarlanan bir API sürümü alma</span><span class="sxs-lookup"><span data-stu-id="d1cd5-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="d1cd5-112">Bu komut belirtilen KIMLIĞE sahip API sürüm kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="d1cd5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="d1cd5-114">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="d1cd5-114">-ApiVersionSetId</span></span>
<span data-ttu-id="d1cd5-115">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-115">API identifier to look for.</span></span>
<span data-ttu-id="d1cd5-116">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="d1cd5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d1cd5-117">-Context</span></span>
<span data-ttu-id="d1cd5-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d1cd5-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cd5-120">-DefaultProfile</span></span>
<span data-ttu-id="d1cd5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cd5-122">CommonParameters</span></span>
<span data-ttu-id="d1cd5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1cd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cd5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1cd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cd5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1cd5-125">INPUTS</span></span>

### <span data-ttu-id="d1cd5-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d1cd5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1cd5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d1cd5-127">System.String</span></span>

## <span data-ttu-id="d1cd5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1cd5-128">OUTPUTS</span></span>

### <span data-ttu-id="d1cd5-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="d1cd5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d1cd5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1cd5-130">NOTES</span></span>

## <span data-ttu-id="d1cd5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1cd5-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1cd5-132">New-Azurermapımanagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="d1cd5-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="d1cd5-133">Remove-Azurermapsananagementapiset</span><span class="sxs-lookup"><span data-stu-id="d1cd5-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="d1cd5-134">Set-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="d1cd5-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
