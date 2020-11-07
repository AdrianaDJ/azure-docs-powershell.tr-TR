---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751177"
---
# <span data-ttu-id="ce65e-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ce65e-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="ce65e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce65e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce65e-103">API sürümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="ce65e-103">Get the API Release.</span></span>

## <span data-ttu-id="ce65e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce65e-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce65e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce65e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce65e-106">**Get-Azapsananagementapırelease** cmdlet 'ı, Azure API yönetim API 'sının bir veya daha fazla sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ce65e-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="ce65e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce65e-107">EXAMPLES</span></span>

### <span data-ttu-id="ce65e-108">Örnek 1: API 'nin tüm sürümlerini alma</span><span class="sxs-lookup"><span data-stu-id="ce65e-108">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contos
```

<span data-ttu-id="ce65e-109">Bu komut, `echo-api` belirtilen bağlam için API 'nin tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ce65e-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="ce65e-110">Örnek 2: belirli bir API sürümünün sürüm bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="ce65e-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="ce65e-111">Bu komut belirtilen ReleaseID ile belirli bir API 'nin sürüm bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ce65e-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="ce65e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce65e-112">PARAMETERS</span></span>

### <span data-ttu-id="ce65e-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ce65e-113">-ApiId</span></span>
<span data-ttu-id="ce65e-114">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ce65e-114">API identifier to look for.</span></span>
<span data-ttu-id="ce65e-115">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="ce65e-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="ce65e-116">-Context</span><span class="sxs-lookup"><span data-stu-id="ce65e-116">-Context</span></span>
<span data-ttu-id="ce65e-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="ce65e-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ce65e-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce65e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ce65e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce65e-119">-DefaultProfile</span></span>
<span data-ttu-id="ce65e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce65e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce65e-121">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="ce65e-121">-ReleaseId</span></span>
<span data-ttu-id="ce65e-122">Sürümün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="ce65e-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="ce65e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce65e-123">CommonParameters</span></span>
<span data-ttu-id="ce65e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce65e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce65e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce65e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce65e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce65e-126">INPUTS</span></span>

### <span data-ttu-id="ce65e-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ce65e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ce65e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ce65e-128">System.String</span></span>

## <span data-ttu-id="ce65e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce65e-129">OUTPUTS</span></span>

### <span data-ttu-id="ce65e-130">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="ce65e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ce65e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce65e-131">NOTES</span></span>

## <span data-ttu-id="ce65e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce65e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce65e-133">Yeni-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="ce65e-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="ce65e-134">Remove-Azapsananagementapırelease</span><span class="sxs-lookup"><span data-stu-id="ce65e-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="ce65e-135">Set-Azapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="ce65e-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)