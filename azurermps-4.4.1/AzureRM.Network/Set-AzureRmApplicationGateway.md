---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595142"
---
# <span data-ttu-id="c3b75-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3b75-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="c3b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b75-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b75-103">Uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3b75-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3b75-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3b75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3b75-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b75-106">**Set-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3b75-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="c3b75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3b75-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b75-108">Örnek 1: uygulama ağ geçidini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c3b75-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c3b75-109">Bu komut, uygulama ağ geçidini $AppGw değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3b75-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="c3b75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3b75-110">PARAMETERS</span></span>

### <span data-ttu-id="c3b75-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3b75-111">-ApplicationGateway</span></span>
<span data-ttu-id="c3b75-112">Uygulama ağ geçidinin ayarlanması gereken durumu temsil eden bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3b75-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b75-113">-DefaultProfile</span></span>
<span data-ttu-id="c3b75-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3b75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3b75-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b75-115">CommonParameters</span></span>
<span data-ttu-id="c3b75-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3b75-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b75-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b75-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b75-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3b75-118">INPUTS</span></span>

### <span data-ttu-id="c3b75-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3b75-119">PSApplicationGateway</span></span>
<span data-ttu-id="c3b75-120">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c3b75-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="c3b75-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3b75-121">OUTPUTS</span></span>

### <span data-ttu-id="c3b75-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3b75-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3b75-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3b75-123">NOTES</span></span>

## <span data-ttu-id="c3b75-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3b75-124">RELATED LINKS</span></span>

[<span data-ttu-id="c3b75-125">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3b75-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


