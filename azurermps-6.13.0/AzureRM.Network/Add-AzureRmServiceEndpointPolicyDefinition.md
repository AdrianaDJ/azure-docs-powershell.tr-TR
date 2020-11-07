---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763829"
---
# <span data-ttu-id="a8329-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8329-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a8329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8329-102">SYNOPSIS</span></span>
<span data-ttu-id="a8329-103">Belirtilen ilkeye hizmet uç noktası ilke tanımı ekler.</span><span class="sxs-lookup"><span data-stu-id="a8329-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8329-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8329-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8329-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8329-105">DESCRIPTION</span></span>
<span data-ttu-id="a8329-106">**Add-AzureRmServiceEndpointPolicyDefinition** cmdlet 'i ilkeye bir hizmet uç noktası ilke tanımı ekler.</span><span class="sxs-lookup"><span data-stu-id="a8329-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="a8329-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8329-107">EXAMPLES</span></span>

### <span data-ttu-id="a8329-108">Örnek 1: hizmet uç noktası ilkesinde hizmet uç noktası İlkesi tanımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a8329-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="a8329-109">Bu komut, ad ServiceEndpointPolicyDefinition1, hizmet Microsoft. Storage, hizmet kaynakları abonelikleri/sub1 ve açıklaması "yeni tanım" olan hizmet uç noktası İlkesi tanımını, ResourceGroup01 adlı kaynak grubuna ait ve $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a8329-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="a8329-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8329-110">PARAMETERS</span></span>

### <span data-ttu-id="a8329-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8329-111">-DefaultProfile</span></span>
<span data-ttu-id="a8329-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8329-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8329-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a8329-113">-Description</span></span>
<span data-ttu-id="a8329-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="a8329-114">The description of the definition</span></span>

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

### <span data-ttu-id="a8329-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8329-115">-Name</span></span>
<span data-ttu-id="a8329-116">Hizmet uç noktası ilke tanımının adı</span><span class="sxs-lookup"><span data-stu-id="a8329-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="a8329-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="a8329-117">-Service</span></span>
<span data-ttu-id="a8329-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="a8329-118">Name of the service</span></span>

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

### <span data-ttu-id="a8329-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8329-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a8329-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8329-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="a8329-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="a8329-121">-ServiceResource</span></span>
<span data-ttu-id="a8329-122">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="a8329-122">List of service resources</span></span>

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

### <span data-ttu-id="a8329-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8329-123">CommonParameters</span></span>
<span data-ttu-id="a8329-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8329-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8329-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8329-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8329-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8329-126">INPUTS</span></span>

### <span data-ttu-id="a8329-127">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8329-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="a8329-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8329-128">OUTPUTS</span></span>

### <span data-ttu-id="a8329-129">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8329-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="a8329-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8329-130">NOTES</span></span>

## <span data-ttu-id="a8329-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8329-131">RELATED LINKS</span></span>
