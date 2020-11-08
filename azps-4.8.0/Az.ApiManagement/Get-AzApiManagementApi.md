---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274208"
---
# <span data-ttu-id="fbb8c-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fbb8c-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="fbb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb8c-103">Bir API alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-103">Gets an API.</span></span>

## <span data-ttu-id="fbb8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbb8c-104">SYNTAX</span></span>

### <span data-ttu-id="fbb8c-105">GetAllApis (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fbb8c-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbb8c-106">Getbyapııd</span><span class="sxs-lookup"><span data-stu-id="fbb8c-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb8c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="fbb8c-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb8c-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="fbb8c-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb8c-109">Getbygatewayıd</span><span class="sxs-lookup"><span data-stu-id="fbb8c-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb8c-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbb8c-110">DESCRIPTION</span></span>
<span data-ttu-id="fbb8c-111">**Get-Azapsananagementapı** cmdlet 'i bir veya daha çok Azure API yönetim API 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="fbb8c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbb8c-112">EXAMPLES</span></span>

### <span data-ttu-id="fbb8c-113">Örnek 1: tüm yönetim API 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="fbb8c-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="fbb8c-114">Bu komut belirtilen bağlam için tüm API 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="fbb8c-115">Örnek 2: KIMLIĞE göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="fbb8c-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="fbb8c-116">Bu komut belirtilen KIMLIĞE sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="fbb8c-117">Örnek 3: ada göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="fbb8c-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="fbb8c-118">Bu komut, belirtilen ada sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="fbb8c-119">Örnek 4: Gatewayıd 'nin Yönetim API 'sini alma</span><span class="sxs-lookup"><span data-stu-id="fbb8c-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="fbb8c-120">Bu komut belirtilen Gatewayıd 'nin API 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="fbb8c-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbb8c-121">PARAMETERS</span></span>

### <span data-ttu-id="fbb8c-122">-Apııd</span><span class="sxs-lookup"><span data-stu-id="fbb8c-122">-ApiId</span></span>
<span data-ttu-id="fbb8c-123">Alınacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="fbb8c-124">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="fbb8c-124">-ApiRevision</span></span>
<span data-ttu-id="fbb8c-125">Belirli API düzeltmesinin düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="fbb8c-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbb8c-127">-Context</span><span class="sxs-lookup"><span data-stu-id="fbb8c-127">-Context</span></span>
<span data-ttu-id="fbb8c-128">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fbb8c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb8c-129">-DefaultProfile</span></span>
<span data-ttu-id="fbb8c-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbb8c-131">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="fbb8c-131">-GatewayId</span></span>
<span data-ttu-id="fbb8c-132">Belirtilmişse tüm ağ geçidi API 'Lerini almayı dener.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb8c-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbb8c-133">-Name</span></span>
<span data-ttu-id="fbb8c-134">Alınacak API 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="fbb8c-135">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="fbb8c-135">-ProductId</span></span>
<span data-ttu-id="fbb8c-136">API alınacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="fbb8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb8c-137">CommonParameters</span></span>
<span data-ttu-id="fbb8c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb8c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fbb8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb8c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbb8c-140">INPUTS</span></span>

### <span data-ttu-id="fbb8c-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fbb8c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fbb8c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb8c-142">System.String</span></span>

## <span data-ttu-id="fbb8c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbb8c-143">OUTPUTS</span></span>

### <span data-ttu-id="fbb8c-144">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fbb8c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fbb8c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbb8c-145">NOTES</span></span>

## <span data-ttu-id="fbb8c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbb8c-146">RELATED LINKS</span></span>

[<span data-ttu-id="fbb8c-147">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fbb8c-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="fbb8c-148">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fbb8c-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="fbb8c-149">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="fbb8c-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="fbb8c-150">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fbb8c-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="fbb8c-151">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fbb8c-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


