---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593203"
---
# <span data-ttu-id="7f3b5-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3b5-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="7f3b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3b5-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="7f3b5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f3b5-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f3b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f3b5-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3b5-106">**Yeni-AzureRmServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="7f3b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f3b5-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3b5-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="7f3b5-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="7f3b5-109">Bu komut, Policy1 adında, nesne $serviceEndpointDefinition tanımlanan tanımlara sahip bir hizmet bitiş noktası ilkesi oluşturur ve $serviceEndpointPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="7f3b5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f3b5-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3b5-111">-DefaultProfile</span></span>
<span data-ttu-id="7f3b5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3b5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7f3b5-113">-Force</span></span>
<span data-ttu-id="7f3b5-114">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="7f3b5-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3b5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f3b5-115">-Name</span></span>
<span data-ttu-id="7f3b5-116">Alt ağın adı</span><span class="sxs-lookup"><span data-stu-id="7f3b5-116">The name of the subnet</span></span>

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

### <span data-ttu-id="7f3b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f3b5-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-118">The resource group name.</span></span>

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

### <span data-ttu-id="7f3b5-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="7f3b5-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="7f3b5-120">Hizmet uç noktası tanımlarının listesi</span><span class="sxs-lookup"><span data-stu-id="7f3b5-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3b5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f3b5-121">-Confirm</span></span>
<span data-ttu-id="7f3b5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f3b5-123">-WhatIf</span></span>
<span data-ttu-id="7f3b5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f3b5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f3b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3b5-126">CommonParameters</span></span>
<span data-ttu-id="7f3b5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f3b5-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3b5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3b5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f3b5-129">INPUTS</span></span>

### <span data-ttu-id="7f3b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3b5-130">System.String</span></span>


## <span data-ttu-id="7f3b5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f3b5-131">OUTPUTS</span></span>

### <span data-ttu-id="7f3b5-132">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3b5-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="7f3b5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f3b5-133">NOTES</span></span>

## <span data-ttu-id="7f3b5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f3b5-134">RELATED LINKS</span></span>
