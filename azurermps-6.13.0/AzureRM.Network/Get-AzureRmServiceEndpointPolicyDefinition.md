---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592761"
---
# <span data-ttu-id="a5bc4-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a5bc4-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a5bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5bc4-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="a5bc4-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5bc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5bc4-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5bc4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="a5bc4-106">**Get-AzureRmServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası İlkesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="a5bc4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="a5bc4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5bc4-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="a5bc4-109">Bu komut, ServiceEndpointPolicy 'da ServiceEndpointPolicyDefinition1 adındaki hizmet uç noktası İlkesi tanımını alır $Policy $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="a5bc4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5bc4-110">PARAMETERS</span></span>

### <span data-ttu-id="a5bc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5bc4-111">-DefaultProfile</span></span>
<span data-ttu-id="a5bc4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5bc4-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5bc4-113">-Name</span></span>
<span data-ttu-id="a5bc4-114">Hizmet uç noktası ilke tanımının adı</span><span class="sxs-lookup"><span data-stu-id="a5bc4-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="a5bc4-115">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5bc4-115">-ResourceId</span></span>
<span data-ttu-id="a5bc4-116">{{Fill RESOURCEID açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a5bc4-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5bc4-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a5bc4-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a5bc4-118">Hizmet bitiş noktası İlkesi</span><span class="sxs-lookup"><span data-stu-id="a5bc4-118">The Service endpoint policy</span></span>

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

### <span data-ttu-id="a5bc4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5bc4-119">-Confirm</span></span>
<span data-ttu-id="a5bc4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bc4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5bc4-121">-WhatIf</span></span>
<span data-ttu-id="a5bc4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5bc4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5bc4-124">CommonParameters</span></span>
<span data-ttu-id="a5bc4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5bc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5bc4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5bc4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5bc4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5bc4-127">INPUTS</span></span>

### <span data-ttu-id="a5bc4-128">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a5bc4-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a5bc4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5bc4-129">OUTPUTS</span></span>

### <span data-ttu-id="a5bc4-130">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a5bc4-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a5bc4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5bc4-131">NOTES</span></span>

## <span data-ttu-id="a5bc4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5bc4-132">RELATED LINKS</span></span>
