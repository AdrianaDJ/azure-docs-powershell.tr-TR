---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278184"
---
# <span data-ttu-id="8862a-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="8862a-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="8862a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8862a-102">SYNOPSIS</span></span>
<span data-ttu-id="8862a-103">İstekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu tutar</span><span class="sxs-lookup"><span data-stu-id="8862a-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="8862a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8862a-104">SYNTAX</span></span>

### <span data-ttu-id="8862a-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8862a-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8862a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8862a-106">DESCRIPTION</span></span>
<span data-ttu-id="8862a-107">Uyarlamalı ağ Hardenings otomatik olarak Azure Güvenlik Merkezi tarafından hesaplandığından, istekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu kılan bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="8862a-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="8862a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8862a-108">EXAMPLES</span></span>

### <span data-ttu-id="8862a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8862a-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="8862a-110">İstekte listelenen NSG 'ler üzerinde verilen kuralları zorunlu tutar</span><span class="sxs-lookup"><span data-stu-id="8862a-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="8862a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8862a-111">PARAMETERS</span></span>

### <span data-ttu-id="8862a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8862a-112">-DefaultProfile</span></span>
<span data-ttu-id="8862a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8862a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8862a-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="8862a-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="8862a-115">Uyarlamalı ağ sağlamlaştırma kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="8862a-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="8862a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8862a-116">-ResourceGroupName</span></span>
<span data-ttu-id="8862a-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8862a-117">Resource group name.</span></span>

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

### <span data-ttu-id="8862a-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8862a-118">-ResourceName</span></span>
<span data-ttu-id="8862a-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8862a-119">Resource name.</span></span>

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

### <span data-ttu-id="8862a-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="8862a-120">-ResourceNamespace</span></span>
<span data-ttu-id="8862a-121">Kaynağın ad alanı.</span><span class="sxs-lookup"><span data-stu-id="8862a-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="8862a-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8862a-122">-ResourceType</span></span>
<span data-ttu-id="8862a-123">Kaynağın türü.</span><span class="sxs-lookup"><span data-stu-id="8862a-123">The type of the resource.</span></span>

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

### <span data-ttu-id="8862a-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8862a-124">-SubscriptionId</span></span>
<span data-ttu-id="8862a-125">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8862a-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="8862a-126">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="8862a-126">-Rules</span></span>
<span data-ttu-id="8862a-127">Uygulanacak kurallar.</span><span class="sxs-lookup"><span data-stu-id="8862a-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="8862a-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="8862a-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="8862a-129">Uyarlamalı ağ sağlamlaştırma kurallarından oluşturulan güvenlik kurallarıyla güncelleştirilecek geçerli ağ güvenliği gruplarının Azure kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="8862a-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="8862a-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8862a-130">-PassThru</span></span>
<span data-ttu-id="8862a-131">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="8862a-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="8862a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8862a-132">CommonParameters</span></span>
<span data-ttu-id="8862a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8862a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8862a-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8862a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8862a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8862a-135">INPUTS</span></span>

### <span data-ttu-id="8862a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8862a-136">System.String</span></span>

### <span data-ttu-id="8862a-137">Microsoft. Azure. Commands. Securitcenter. modeller. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="8862a-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="8862a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8862a-138">OUTPUTS</span></span>

### <span data-ttu-id="8862a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8862a-139">System.Boolean</span></span>

## <span data-ttu-id="8862a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8862a-140">NOTES</span></span>

## <span data-ttu-id="8862a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8862a-141">RELATED LINKS</span></span>