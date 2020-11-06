---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587347"
---
# <span data-ttu-id="34d6d-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="34d6d-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="34d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="34d6d-103">Bir API alır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34d6d-104">SYNTAX</span></span>

### <span data-ttu-id="34d6d-105">GetAllApis (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34d6d-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34d6d-106">Getbyapııd</span><span class="sxs-lookup"><span data-stu-id="34d6d-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34d6d-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="34d6d-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34d6d-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="34d6d-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34d6d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="34d6d-109">DESCRIPTION</span></span>
<span data-ttu-id="34d6d-110">**Get-Azurermapımanagementapı** cmdlet 'i bir veya daha çok Azure API yönetim API 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="34d6d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34d6d-111">EXAMPLES</span></span>

### <span data-ttu-id="34d6d-112">Örnek 1: tüm yönetim API 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="34d6d-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="34d6d-113">Bu komut belirtilen bağlam için tüm API 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="34d6d-114">Örnek 2: KIMLIĞE göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="34d6d-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="34d6d-115">Bu komut belirtilen KIMLIĞE sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="34d6d-116">Örnek 3: ada göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="34d6d-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="34d6d-117">Bu komut, belirtilen ada sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="34d6d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34d6d-118">PARAMETERS</span></span>

### <span data-ttu-id="34d6d-119">-Apııd</span><span class="sxs-lookup"><span data-stu-id="34d6d-119">-ApiId</span></span>
<span data-ttu-id="34d6d-120">Alınacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34d6d-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="34d6d-121">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="34d6d-121">-ApiRevision</span></span>
<span data-ttu-id="34d6d-122">Belirli API düzeltmesinin düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="34d6d-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="34d6d-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="34d6d-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="34d6d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="34d6d-124">-Context</span></span>
<span data-ttu-id="34d6d-125">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34d6d-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="34d6d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d6d-126">-DefaultProfile</span></span>
<span data-ttu-id="34d6d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34d6d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d6d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="34d6d-128">-Name</span></span>
<span data-ttu-id="34d6d-129">Alınacak API 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34d6d-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="34d6d-130">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="34d6d-130">-ProductId</span></span>
<span data-ttu-id="34d6d-131">API alınacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34d6d-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="34d6d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d6d-132">CommonParameters</span></span>
<span data-ttu-id="34d6d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34d6d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d6d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d6d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d6d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34d6d-135">INPUTS</span></span>

### <span data-ttu-id="34d6d-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="34d6d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34d6d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="34d6d-137">System.String</span></span>

## <span data-ttu-id="34d6d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34d6d-138">OUTPUTS</span></span>

### <span data-ttu-id="34d6d-139">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="34d6d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34d6d-140">NOTES</span></span>

## <span data-ttu-id="34d6d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34d6d-141">RELATED LINKS</span></span>

[<span data-ttu-id="34d6d-142">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="34d6d-143">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="34d6d-144">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="34d6d-145">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="34d6d-146">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="34d6d-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


