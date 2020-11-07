---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 3e5b928696fde62a9628a055191d0aabf94b5311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931940"
---
# <span data-ttu-id="37f07-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="37f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f07-102">SYNOPSIS</span></span>
<span data-ttu-id="37f07-103">Http durum koduyla özel hata oluşturur ve özel hata sayfası URL 'si</span><span class="sxs-lookup"><span data-stu-id="37f07-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="37f07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37f07-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37f07-105">DESCRIPTION</span></span>
<span data-ttu-id="37f07-106">**Yeni-AzApplicationGatewayCustomError** cmdlet 'i özel bir hata oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37f07-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="37f07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37f07-107">EXAMPLES</span></span>

### <span data-ttu-id="37f07-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37f07-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="37f07-109">Bu komut http durum kodu 403 özel hatasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37f07-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="37f07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37f07-110">PARAMETERS</span></span>

### <span data-ttu-id="37f07-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="37f07-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="37f07-112">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="37f07-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37f07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f07-113">-DefaultProfile</span></span>
<span data-ttu-id="37f07-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37f07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f07-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="37f07-115">-StatusCode</span></span>
<span data-ttu-id="37f07-116">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="37f07-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37f07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f07-117">CommonParameters</span></span>
<span data-ttu-id="37f07-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37f07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f07-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f07-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f07-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37f07-120">INPUTS</span></span>

### <span data-ttu-id="37f07-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37f07-121">None</span></span>

## <span data-ttu-id="37f07-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37f07-122">OUTPUTS</span></span>

### <span data-ttu-id="37f07-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="37f07-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37f07-124">NOTES</span></span>

## <span data-ttu-id="37f07-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37f07-125">RELATED LINKS</span></span>

[<span data-ttu-id="37f07-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f07-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f07-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f07-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f07-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
