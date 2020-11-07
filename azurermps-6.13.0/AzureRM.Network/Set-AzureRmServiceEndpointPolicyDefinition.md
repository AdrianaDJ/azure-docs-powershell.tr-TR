---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762914"
---
# <span data-ttu-id="45129-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="45129-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="45129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45129-102">SYNOPSIS</span></span>
<span data-ttu-id="45129-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="45129-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45129-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45129-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45129-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45129-105">DESCRIPTION</span></span>
<span data-ttu-id="45129-106">**Set-AzureRmServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45129-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="45129-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45129-107">EXAMPLES</span></span>

### <span data-ttu-id="45129-108">Örnek 1: hizmet uç noktası ilkesinde hizmet uç noktası İlkesi tanımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="45129-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="45129-109">Bu komut, nesne $ServiceEndpointPolicy tarafından tanımlanan hizmet uç noktası ilkesinde Policydef1 adlı bir hizmet uç noktası İlkesi tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="45129-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="45129-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45129-110">PARAMETERS</span></span>

### <span data-ttu-id="45129-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45129-111">-DefaultProfile</span></span>
<span data-ttu-id="45129-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45129-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45129-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="45129-113">-Description</span></span>
<span data-ttu-id="45129-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="45129-114">The description of the definition</span></span>

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

### <span data-ttu-id="45129-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="45129-115">-Name</span></span>
<span data-ttu-id="45129-116">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="45129-116">The name of the rule</span></span>

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

### <span data-ttu-id="45129-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="45129-117">-Service</span></span>
<span data-ttu-id="45129-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="45129-118">Name of the service</span></span>

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

### <span data-ttu-id="45129-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="45129-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="45129-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="45129-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="45129-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="45129-121">-ServiceResource</span></span>
<span data-ttu-id="45129-122">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="45129-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45129-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45129-123">CommonParameters</span></span>
<span data-ttu-id="45129-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45129-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="45129-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45129-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45129-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45129-126">INPUTS</span></span>

### <span data-ttu-id="45129-127">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="45129-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="45129-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45129-128">OUTPUTS</span></span>

### <span data-ttu-id="45129-129">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="45129-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="45129-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45129-130">NOTES</span></span>

## <span data-ttu-id="45129-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45129-131">RELATED LINKS</span></span>
