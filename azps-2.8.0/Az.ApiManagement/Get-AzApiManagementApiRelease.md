---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 19395960d3a0026b7a14c4ca8232c18d511af989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753605"
---
# <span data-ttu-id="11807-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="11807-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="11807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11807-102">SYNOPSIS</span></span>
<span data-ttu-id="11807-103">API sürümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="11807-103">Get the API Release.</span></span>

## <span data-ttu-id="11807-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11807-104">SYNTAX</span></span>

### <span data-ttu-id="11807-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11807-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11807-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="11807-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11807-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="11807-107">DESCRIPTION</span></span>
<span data-ttu-id="11807-108">**Get-Azapsananagementapırelease** cmdlet 'ı, Azure API yönetim API 'sının bir veya daha fazla sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="11807-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="11807-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11807-109">EXAMPLES</span></span>

### <span data-ttu-id="11807-110">Örnek 1: API 'nin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="11807-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="11807-111">Bu komut, `echo-api` belirtilen bağlam için API 'nin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="11807-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="11807-112">Örnek 2: belirli bir API sürümünün sürüm bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="11807-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="11807-113">Bu komut belirtilen ReleaseID ile belirli bir API 'nin sürüm bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="11807-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="11807-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11807-114">PARAMETERS</span></span>

### <span data-ttu-id="11807-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="11807-115">-ApiId</span></span>
<span data-ttu-id="11807-116">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="11807-116">API identifier to look for.</span></span>
<span data-ttu-id="11807-117">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="11807-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="11807-118">-Context</span><span class="sxs-lookup"><span data-stu-id="11807-118">-Context</span></span>
<span data-ttu-id="11807-119">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="11807-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="11807-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="11807-120">This parameter is required.</span></span>

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

### <span data-ttu-id="11807-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11807-121">-DefaultProfile</span></span>
<span data-ttu-id="11807-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11807-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11807-123">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="11807-123">-ReleaseId</span></span>
<span data-ttu-id="11807-124">Sürümün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="11807-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="11807-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="11807-125">-ResourceId</span></span>
<span data-ttu-id="11807-126">Bir API sürümünün ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="11807-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="11807-127">Belirtilirse, tanımlayıcı tarafından API 'yi bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="11807-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="11807-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="11807-128">This parameter is required.</span></span>

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

### <span data-ttu-id="11807-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11807-129">CommonParameters</span></span>
<span data-ttu-id="11807-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11807-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11807-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="11807-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11807-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11807-132">INPUTS</span></span>

### <span data-ttu-id="11807-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="11807-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="11807-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11807-134">System.String</span></span>

## <span data-ttu-id="11807-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11807-135">OUTPUTS</span></span>

### <span data-ttu-id="11807-136">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="11807-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="11807-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11807-137">NOTES</span></span>

## <span data-ttu-id="11807-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11807-138">RELATED LINKS</span></span>

[<span data-ttu-id="11807-139">Yeni-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="11807-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="11807-140">Remove-Azapsananagementapırelease</span><span class="sxs-lookup"><span data-stu-id="11807-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="11807-141">Set-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="11807-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)