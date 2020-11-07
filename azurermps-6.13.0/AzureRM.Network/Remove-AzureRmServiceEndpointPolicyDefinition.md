---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593953"
---
# <span data-ttu-id="2903f-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2903f-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="2903f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2903f-102">SYNOPSIS</span></span>
<span data-ttu-id="2903f-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="2903f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2903f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2903f-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2903f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2903f-105">DESCRIPTION</span></span>
<span data-ttu-id="2903f-106">**Remove-AzureRmServiceEndpointPolicy** cmdlet 'i, hizmet uç nokta ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2903f-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="2903f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2903f-107">EXAMPLES</span></span>

### <span data-ttu-id="2903f-108">Örnek 1: ad kullanan bir hizmet uç nokta ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="2903f-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="2903f-109">Bu komut, ad</span><span class="sxs-lookup"><span data-stu-id="2903f-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="2903f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2903f-110">PARAMETERS</span></span>

### <span data-ttu-id="2903f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2903f-111">-DefaultProfile</span></span>
<span data-ttu-id="2903f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2903f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2903f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2903f-113">-Name</span></span>
<span data-ttu-id="2903f-114">Hizmet uç noktası tanımının adı</span><span class="sxs-lookup"><span data-stu-id="2903f-114">The name of the service endpoint definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2903f-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2903f-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2903f-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2903f-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="2903f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2903f-117">CommonParameters</span></span>
<span data-ttu-id="2903f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2903f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2903f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2903f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2903f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2903f-120">INPUTS</span></span>

### <span data-ttu-id="2903f-121">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2903f-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2903f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2903f-122">OUTPUTS</span></span>

### <span data-ttu-id="2903f-123">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2903f-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2903f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2903f-124">NOTES</span></span>

## <span data-ttu-id="2903f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2903f-125">RELATED LINKS</span></span>