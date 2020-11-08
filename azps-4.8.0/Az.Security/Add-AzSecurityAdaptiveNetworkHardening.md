---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266384"
---
# <span data-ttu-id="10f13-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="10f13-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="10f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f13-102">SYNOPSIS</span></span>
<span data-ttu-id="10f13-103">İstekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu tutar</span><span class="sxs-lookup"><span data-stu-id="10f13-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="10f13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10f13-104">SYNTAX</span></span>

### <span data-ttu-id="10f13-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10f13-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10f13-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="10f13-106">DESCRIPTION</span></span>
<span data-ttu-id="10f13-107">Uyarlamalı ağ Hardenings otomatik olarak Azure Güvenlik Merkezi tarafından hesaplandığından, istekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu kılan bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="10f13-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="10f13-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10f13-108">EXAMPLES</span></span>

### <span data-ttu-id="10f13-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10f13-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="10f13-110">İstekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu tutar</span><span class="sxs-lookup"><span data-stu-id="10f13-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="10f13-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10f13-111">PARAMETERS</span></span>

### <span data-ttu-id="10f13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f13-112">-DefaultProfile</span></span>
<span data-ttu-id="10f13-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10f13-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10f13-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="10f13-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="10f13-115">Uyarlamalı ağ sağlamlaştırma kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="10f13-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f13-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f13-116">-ResourceGroupName</span></span>
<span data-ttu-id="10f13-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="10f13-117">Resource group name.</span></span>

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

### <span data-ttu-id="10f13-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="10f13-118">-ResourceName</span></span>
<span data-ttu-id="10f13-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="10f13-119">Resource name.</span></span>

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

### <span data-ttu-id="10f13-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="10f13-120">-ResourceNamespace</span></span>
<span data-ttu-id="10f13-121">Kaynağın ad alanı.</span><span class="sxs-lookup"><span data-stu-id="10f13-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="10f13-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="10f13-122">-ResourceType</span></span>
<span data-ttu-id="10f13-123">Kaynağın türü.</span><span class="sxs-lookup"><span data-stu-id="10f13-123">The type of the resource.</span></span>

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

### <span data-ttu-id="10f13-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="10f13-124">-SubscriptionId</span></span>
<span data-ttu-id="10f13-125">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="10f13-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f13-126">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="10f13-126">-Rules</span></span>
<span data-ttu-id="10f13-127">Uygulanacak kurallar.</span><span class="sxs-lookup"><span data-stu-id="10f13-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10f13-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="10f13-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="10f13-129">Uyarlamalı ağ sağlamlaştırma kurallarından oluşturulan güvenlik kurallarıyla güncelleştirilecek geçerli ağ güvenliği gruplarının Azure kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="10f13-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f13-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="10f13-130">-PassThru</span></span>
<span data-ttu-id="10f13-131">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="10f13-131">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f13-132">CommonParameters</span></span>
<span data-ttu-id="10f13-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10f13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f13-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f13-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f13-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10f13-135">INPUTS</span></span>

### <span data-ttu-id="10f13-136">System. String</span><span class="sxs-lookup"><span data-stu-id="10f13-136">System.String</span></span>

### <span data-ttu-id="10f13-137">Microsoft. Azure. Commands. Securitcenter. modeller. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="10f13-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="10f13-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10f13-138">OUTPUTS</span></span>

### <span data-ttu-id="10f13-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10f13-139">System.Boolean</span></span>

## <span data-ttu-id="10f13-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10f13-140">NOTES</span></span>

## <span data-ttu-id="10f13-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10f13-141">RELATED LINKS</span></span>