---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593199"
---
# <span data-ttu-id="ef1c1-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef1c1-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ef1c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1c1-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="ef1c1-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef1c1-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef1c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef1c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1c1-106">**Yeni-AzureRmServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ef1c1-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="ef1c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef1c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ef1c1-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="ef1c1-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="ef1c1-109">Bu komut, ad ServiceEndpointPolicyDefinition1, hizmet Microsoft. Storage, hizmet kaynakları abonelikleri/sub1 ve açıklaması "yeni tanım" olan ve ResourceGroup01 adlı kaynak grubuna ait olan hizmet uç noktası İlkesi tanımını oluşturur ve $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ef1c1-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="ef1c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef1c1-110">PARAMETERS</span></span>

### <span data-ttu-id="ef1c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1c1-111">-DefaultProfile</span></span>
<span data-ttu-id="ef1c1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef1c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef1c1-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ef1c1-113">-Description</span></span>
<span data-ttu-id="ef1c1-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="ef1c1-114">The description of the definition</span></span>

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

### <span data-ttu-id="ef1c1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef1c1-115">-Name</span></span>
<span data-ttu-id="ef1c1-116">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="ef1c1-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="ef1c1-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="ef1c1-117">-Service</span></span>
<span data-ttu-id="ef1c1-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="ef1c1-118">Name of the service</span></span>

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

### <span data-ttu-id="ef1c1-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="ef1c1-119">-ServiceResource</span></span>
<span data-ttu-id="ef1c1-120">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="ef1c1-120">List of service resources</span></span>

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

### <span data-ttu-id="ef1c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1c1-121">CommonParameters</span></span>
<span data-ttu-id="ef1c1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef1c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef1c1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1c1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1c1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef1c1-124">INPUTS</span></span>

### <span data-ttu-id="ef1c1-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ef1c1-125">None</span></span>


## <span data-ttu-id="ef1c1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef1c1-126">OUTPUTS</span></span>

### <span data-ttu-id="ef1c1-127">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef1c1-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="ef1c1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef1c1-128">NOTES</span></span>

## <span data-ttu-id="ef1c1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef1c1-129">RELATED LINKS</span></span>
