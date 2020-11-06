---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593205"
---
# <span data-ttu-id="21fce-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="21fce-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="21fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fce-102">SYNOPSIS</span></span>
<span data-ttu-id="21fce-103">Http durum koduyla özel hata oluşturur ve özel hata sayfası URL 'si</span><span class="sxs-lookup"><span data-stu-id="21fce-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21fce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21fce-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21fce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21fce-105">DESCRIPTION</span></span>
<span data-ttu-id="21fce-106">**New-AzureRmApplicationGatewayCustomError** cmdlet 'i özel bir hata oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21fce-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="21fce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21fce-107">EXAMPLES</span></span>

### <span data-ttu-id="21fce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21fce-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="21fce-109">Bu komut http durum kodu 403 özel hatasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21fce-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="21fce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21fce-110">PARAMETERS</span></span>

### <span data-ttu-id="21fce-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="21fce-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="21fce-112">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="21fce-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fce-113">-DefaultProfile</span></span>
<span data-ttu-id="21fce-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21fce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fce-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="21fce-115">-StatusCode</span></span>
<span data-ttu-id="21fce-116">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="21fce-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fce-117">CommonParameters</span></span>
<span data-ttu-id="21fce-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21fce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21fce-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21fce-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fce-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21fce-120">INPUTS</span></span>

### <span data-ttu-id="21fce-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21fce-121">None</span></span>

## <span data-ttu-id="21fce-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21fce-122">OUTPUTS</span></span>

### <span data-ttu-id="21fce-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="21fce-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="21fce-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21fce-124">NOTES</span></span>

## <span data-ttu-id="21fce-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21fce-125">RELATED LINKS</span></span>
