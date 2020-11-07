---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762915"
---
# <span data-ttu-id="ceff1-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ceff1-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="ceff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceff1-102">SYNOPSIS</span></span>
<span data-ttu-id="ceff1-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="ceff1-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceff1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ceff1-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceff1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ceff1-105">DESCRIPTION</span></span>
<span data-ttu-id="ceff1-106">**Set-AzureRmServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ceff1-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="ceff1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ceff1-107">EXAMPLES</span></span>

### <span data-ttu-id="ceff1-108">Örnek 1: hizmet uç noktası ilkesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="ceff1-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ceff1-109">Bu komut, nesne $serviceEndpointPolicy tanımlanan Policy1 adlı bir hizmet ana</span><span class="sxs-lookup"><span data-stu-id="ceff1-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="ceff1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ceff1-110">PARAMETERS</span></span>

### <span data-ttu-id="ceff1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceff1-111">-DefaultProfile</span></span>
<span data-ttu-id="ceff1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ceff1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceff1-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ceff1-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ceff1-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ceff1-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceff1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceff1-115">CommonParameters</span></span>
<span data-ttu-id="ceff1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ceff1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ceff1-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceff1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceff1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ceff1-118">INPUTS</span></span>

### <span data-ttu-id="ceff1-119">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ceff1-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="ceff1-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ceff1-120">OUTPUTS</span></span>

### <span data-ttu-id="ceff1-121">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ceff1-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="ceff1-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ceff1-122">NOTES</span></span>

## <span data-ttu-id="ceff1-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ceff1-123">RELATED LINKS</span></span>
