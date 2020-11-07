---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764287"
---
# <span data-ttu-id="105b5-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="105b5-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="105b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105b5-102">SYNOPSIS</span></span>
<span data-ttu-id="105b5-103">Bir API alır.</span><span class="sxs-lookup"><span data-stu-id="105b5-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="105b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="105b5-104">SYNTAX</span></span>

### <span data-ttu-id="105b5-105">Tüm API 'Ler (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="105b5-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="105b5-106">KIMLIĞE göre bul</span><span class="sxs-lookup"><span data-stu-id="105b5-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105b5-107">Ada göre bul</span><span class="sxs-lookup"><span data-stu-id="105b5-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105b5-108">Ürün KIMLIĞINE göre bulma</span><span class="sxs-lookup"><span data-stu-id="105b5-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="105b5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="105b5-109">DESCRIPTION</span></span>
<span data-ttu-id="105b5-110">**Get-Azurermapımanagementapı** cmdlet 'i bir veya daha çok Azure API yönetim API 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="105b5-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="105b5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="105b5-111">EXAMPLES</span></span>

### <span data-ttu-id="105b5-112">Örnek 1: tüm yönetim API 'Lerini alma</span><span class="sxs-lookup"><span data-stu-id="105b5-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="105b5-113">Bu komut belirtilen bağlam için tüm API 'Leri alır.</span><span class="sxs-lookup"><span data-stu-id="105b5-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="105b5-114">Örnek 2: KIMLIĞE göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="105b5-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="105b5-115">Bu komut belirtilen KIMLIĞE sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="105b5-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="105b5-116">Örnek 3: ada göre bir yönetim API 'SI alma</span><span class="sxs-lookup"><span data-stu-id="105b5-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="105b5-117">Bu komut, belirtilen ada sahip API 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="105b5-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="105b5-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="105b5-118">PARAMETERS</span></span>

### <span data-ttu-id="105b5-119">-Apııd</span><span class="sxs-lookup"><span data-stu-id="105b5-119">-ApiId</span></span>
<span data-ttu-id="105b5-120">Alınacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="105b5-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="105b5-121">-Context</span></span>
<span data-ttu-id="105b5-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="105b5-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="105b5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="105b5-123">-Name</span></span>
<span data-ttu-id="105b5-124">Alınacak API 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="105b5-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b5-125">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="105b5-125">-ProductId</span></span>
<span data-ttu-id="105b5-126">API alınacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="105b5-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105b5-127">-DefaultProfile</span></span>
<span data-ttu-id="105b5-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="105b5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="105b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105b5-129">CommonParameters</span></span>
<span data-ttu-id="105b5-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="105b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105b5-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105b5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105b5-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="105b5-132">INPUTS</span></span>

## <span data-ttu-id="105b5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="105b5-133">OUTPUTS</span></span>

### <span data-ttu-id="105b5-134">IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı></span><span class="sxs-lookup"><span data-stu-id="105b5-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="105b5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="105b5-135">NOTES</span></span>

## <span data-ttu-id="105b5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="105b5-136">RELATED LINKS</span></span>

[<span data-ttu-id="105b5-137">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="105b5-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="105b5-138">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="105b5-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="105b5-139">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="105b5-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="105b5-140">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="105b5-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="105b5-141">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="105b5-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


