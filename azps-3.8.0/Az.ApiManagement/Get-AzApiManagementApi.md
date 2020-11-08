---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 7ec3eacc32157b833095522bbebc76f3838ae2a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097433"
---
# <span data-ttu-id="e886c-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e886c-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="e886c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e886c-102">SYNOPSIS</span></span>
<span data-ttu-id="e886c-103">Bir API alır.</span><span class="sxs-lookup"><span data-stu-id="e886c-103">Gets an API.</span></span>

## <span data-ttu-id="e886c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e886c-104">SYNTAX</span></span>

### <span data-ttu-id="e886c-105">GetAllApis (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e886c-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e886c-106">Getbyapııd</span><span class="sxs-lookup"><span data-stu-id="e886c-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e886c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e886c-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e886c-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="e886c-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e886c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e886c-109">DESCRIPTION</span></span>
<span data-ttu-id="e886c-110">**Get-Azapsananagementapı** cmdlet 'i bir veya daha çok Azure API yönetim API 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="e886c-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="e886c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e886c-111">EXAMPLES</span></span>

### <span data-ttu-id="e886c-112">Örnek 1: tüm yönetim API 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="e886c-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="e886c-113">Bu komut belirtilen bağlam için tüm API 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="e886c-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="e886c-114">Örnek 2: KIMLIĞE göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="e886c-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="e886c-115">Bu komut belirtilen KIMLIĞE sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="e886c-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="e886c-116">Örnek 3: ada göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="e886c-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="e886c-117">Bu komut, belirtilen ada sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="e886c-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="e886c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e886c-118">PARAMETERS</span></span>

### <span data-ttu-id="e886c-119">-Apııd</span><span class="sxs-lookup"><span data-stu-id="e886c-119">-ApiId</span></span>
<span data-ttu-id="e886c-120">Alınacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e886c-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e886c-121">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="e886c-121">-ApiRevision</span></span>
<span data-ttu-id="e886c-122">Belirli API düzeltmesinin düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e886c-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="e886c-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e886c-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e886c-124">-Context</span><span class="sxs-lookup"><span data-stu-id="e886c-124">-Context</span></span>
<span data-ttu-id="e886c-125">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e886c-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e886c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e886c-126">-DefaultProfile</span></span>
<span data-ttu-id="e886c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e886c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e886c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e886c-128">-Name</span></span>
<span data-ttu-id="e886c-129">Alınacak API 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e886c-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e886c-130">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="e886c-130">-ProductId</span></span>
<span data-ttu-id="e886c-131">API alınacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e886c-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e886c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e886c-132">CommonParameters</span></span>
<span data-ttu-id="e886c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e886c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e886c-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e886c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e886c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e886c-135">INPUTS</span></span>

### <span data-ttu-id="e886c-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e886c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e886c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e886c-137">System.String</span></span>

## <span data-ttu-id="e886c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e886c-138">OUTPUTS</span></span>

### <span data-ttu-id="e886c-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e886c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e886c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e886c-140">NOTES</span></span>

## <span data-ttu-id="e886c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e886c-141">RELATED LINKS</span></span>

[<span data-ttu-id="e886c-142">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e886c-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="e886c-143">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e886c-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e886c-144">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="e886c-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e886c-145">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e886c-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e886c-146">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e886c-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


