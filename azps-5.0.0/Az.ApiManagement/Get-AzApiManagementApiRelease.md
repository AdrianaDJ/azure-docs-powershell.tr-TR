---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324094"
---
# <span data-ttu-id="e3d9b-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e3d9b-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="e3d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d9b-103">API sürümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-103">Get the API Release.</span></span>

## <span data-ttu-id="e3d9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3d9b-104">SYNTAX</span></span>

### <span data-ttu-id="e3d9b-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3d9b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3d9b-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e3d9b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3d9b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3d9b-107">DESCRIPTION</span></span>
<span data-ttu-id="e3d9b-108">**Get-Azapsananagementapırelease** cmdlet 'ı, Azure API yönetim API 'sının bir veya daha fazla sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="e3d9b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3d9b-109">EXAMPLES</span></span>

### <span data-ttu-id="e3d9b-110">Örnek 1: API 'nin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="e3d9b-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e3d9b-111">Bu komut, `echo-api` belirtilen bağlam için API 'nin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="e3d9b-112">Örnek 2: belirli bir API sürümünün sürüm bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="e3d9b-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e3d9b-113">Bu komut belirtilen ReleaseID ile belirli bir API 'nin sürüm bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="e3d9b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3d9b-114">PARAMETERS</span></span>

### <span data-ttu-id="e3d9b-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="e3d9b-115">-ApiId</span></span>
<span data-ttu-id="e3d9b-116">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-116">API identifier to look for.</span></span>
<span data-ttu-id="e3d9b-117">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d9b-118">-Context</span><span class="sxs-lookup"><span data-stu-id="e3d9b-118">-Context</span></span>
<span data-ttu-id="e3d9b-119">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e3d9b-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d9b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d9b-121">-DefaultProfile</span></span>
<span data-ttu-id="e3d9b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d9b-123">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="e3d9b-123">-ReleaseId</span></span>
<span data-ttu-id="e3d9b-124">Sürümün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d9b-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e3d9b-125">-ResourceId</span></span>
<span data-ttu-id="e3d9b-126">Bir API sürümünün ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="e3d9b-127">Belirtilirse, tanımlayıcı tarafından API 'yi bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="e3d9b-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-128">This parameter is required.</span></span>

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

### <span data-ttu-id="e3d9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d9b-129">CommonParameters</span></span>
<span data-ttu-id="e3d9b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d9b-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3d9b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d9b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3d9b-132">INPUTS</span></span>

### <span data-ttu-id="e3d9b-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e3d9b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e3d9b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e3d9b-134">System.String</span></span>

## <span data-ttu-id="e3d9b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3d9b-135">OUTPUTS</span></span>

### <span data-ttu-id="e3d9b-136">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="e3d9b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e3d9b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3d9b-137">NOTES</span></span>

## <span data-ttu-id="e3d9b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3d9b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e3d9b-139">Yeni-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="e3d9b-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="e3d9b-140">Remove-Azapsananagementapırelease</span><span class="sxs-lookup"><span data-stu-id="e3d9b-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="e3d9b-141">Güncelleştirme-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="e3d9b-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)