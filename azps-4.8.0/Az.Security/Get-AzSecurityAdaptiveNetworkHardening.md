---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265775"
---
# <span data-ttu-id="7428c-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="7428c-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="7428c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7428c-102">SYNOPSIS</span></span>
<span data-ttu-id="7428c-103">Genişletilmiş kaynağın kapsamındaki Uyarlamalı ağ Hardenings kaynaklarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7428c-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="7428c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7428c-104">SYNTAX</span></span>

### <span data-ttu-id="7428c-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="7428c-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="7428c-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="7428c-106">DESCRIPTION</span></span>
<span data-ttu-id="7428c-107">Uyarlamalı ağ Hardenings otomatik olarak Azure Güvenlik Merkezi tarafından hesaplanır, genişletilmiş bir kaynağın kapsamındaki Uyarlamalı ağ Hardenings kaynaklarının listesini almak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="7428c-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="7428c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7428c-108">EXAMPLES</span></span>

### <span data-ttu-id="7428c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7428c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="7428c-110">Genişletilmiş kaynağın kapsamındaki Uyarlamalı ağ Hardenings kaynaklarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7428c-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="7428c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7428c-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="7428c-112">Tek bir uyarlamalı ağ Hardenings kaynağı edinme</span><span class="sxs-lookup"><span data-stu-id="7428c-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="7428c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7428c-113">PARAMETERS</span></span>

### <span data-ttu-id="7428c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7428c-114">-DefaultProfile</span></span>
<span data-ttu-id="7428c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7428c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7428c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7428c-116">-ResourceGroupName</span></span>
<span data-ttu-id="7428c-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7428c-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7428c-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7428c-118">-ResourceName</span></span>
<span data-ttu-id="7428c-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7428c-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7428c-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="7428c-120">-ResourceNamespace</span></span>
<span data-ttu-id="7428c-121">Kaynağın ad alanı.</span><span class="sxs-lookup"><span data-stu-id="7428c-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7428c-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7428c-122">-ResourceType</span></span>
<span data-ttu-id="7428c-123">Kaynağın türü.</span><span class="sxs-lookup"><span data-stu-id="7428c-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7428c-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="7428c-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="7428c-125">Uyarlamalı ağ sağlamlaştırma kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="7428c-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7428c-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7428c-126">-SubscriptionId</span></span>
<span data-ttu-id="7428c-127">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7428c-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="7428c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7428c-128">CommonParameters</span></span>
<span data-ttu-id="7428c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7428c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7428c-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7428c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7428c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7428c-131">INPUTS</span></span>

### <span data-ttu-id="7428c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7428c-132">System.String</span></span>

## <span data-ttu-id="7428c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7428c-133">OUTPUTS</span></span>

### <span data-ttu-id="7428c-134">Microsoft. Azure. Commands. Security. modeller. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="7428c-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="7428c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7428c-135">NOTES</span></span>

## <span data-ttu-id="7428c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7428c-136">RELATED LINKS</span></span>