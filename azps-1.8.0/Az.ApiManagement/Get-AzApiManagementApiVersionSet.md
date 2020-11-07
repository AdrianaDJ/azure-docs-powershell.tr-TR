---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751173"
---
# <span data-ttu-id="c3c6f-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3c6f-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c3c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c6f-103">API sürüm kümelerinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="c3c6f-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="c3c6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3c6f-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c6f-106">**Get-Azapsananagementapıversionset** cmdlet 'ı, API yönetim BAĞLAMıNDA yapılandırılmış API sürüm kümelerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="c3c6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="c3c6f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3c6f-108">Example 1</span></span>

### <span data-ttu-id="c3c6f-109">Örnek 1: tüm API sürüm kümelerini alma</span><span class="sxs-lookup"><span data-stu-id="c3c6f-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="c3c6f-110">Bu komut, belirtilen bağlam için tüm API sürüm kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="c3c6f-111">Örnek 2: KIMLIĞE göre ayarlanan bir API sürümü alma</span><span class="sxs-lookup"><span data-stu-id="c3c6f-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="c3c6f-112">Bu komut belirtilen KIMLIĞE sahip API sürüm kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="c3c6f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3c6f-113">PARAMETERS</span></span>

### <span data-ttu-id="c3c6f-114">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="c3c6f-114">-ApiVersionSetId</span></span>
<span data-ttu-id="c3c6f-115">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-115">API identifier to look for.</span></span>
<span data-ttu-id="c3c6f-116">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c3c6f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c3c6f-117">-Context</span></span>
<span data-ttu-id="c3c6f-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c3c6f-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c3c6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c6f-120">-DefaultProfile</span></span>
<span data-ttu-id="c3c6f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c6f-122">CommonParameters</span></span>
<span data-ttu-id="c3c6f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3c6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c6f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c6f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c6f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3c6f-125">INPUTS</span></span>

### <span data-ttu-id="c3c6f-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c3c6f-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3c6f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c6f-127">System.String</span></span>

## <span data-ttu-id="c3c6f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3c6f-128">OUTPUTS</span></span>

### <span data-ttu-id="c3c6f-129">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="c3c6f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c3c6f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3c6f-130">NOTES</span></span>

## <span data-ttu-id="c3c6f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3c6f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c3c6f-132">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="c3c6f-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c3c6f-133">Remove-Azapsananagementapiset</span><span class="sxs-lookup"><span data-stu-id="c3c6f-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c3c6f-134">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="c3c6f-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
