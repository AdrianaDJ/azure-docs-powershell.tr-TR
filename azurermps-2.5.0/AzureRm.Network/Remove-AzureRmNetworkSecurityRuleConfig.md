---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 9aed668c977fc1156e2a52723273b1d6d37fba71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939505"
---
# <span data-ttu-id="58e84-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58e84-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="58e84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e84-102">SYNOPSIS</span></span>
<span data-ttu-id="58e84-103">Ağ güvenlik grubundan bir ağ güvenliği kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58e84-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58e84-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58e84-105">DESCRIPTION</span></span>
<span data-ttu-id="58e84-106">**Remove-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubundan ağ güvenliği kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58e84-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="58e84-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58e84-107">EXAMPLES</span></span>

### <span data-ttu-id="58e84-108">Örnek 1: ağ güvenlik kuralı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="58e84-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="58e84-109">İlk komut, RDP kuralı adlı bir ağ güvenlik kuralı yapılandırması oluşturur ve $rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="58e84-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="58e84-110">İkinci komut $rule 1 ' deki kuralı kullanarak bir ağ güvenlik grubu oluşturur ve ardından ağ güvenlik grubunu $nsg değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="58e84-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="58e84-111">Üçüncü komut, $nsg 'daki ağ güvenliği grubundan RDP-kuralı adlı ağ güvenlik kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58e84-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="58e84-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58e84-112">PARAMETERS</span></span>

### <span data-ttu-id="58e84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e84-113">-DefaultProfile</span></span>
<span data-ttu-id="58e84-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58e84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e84-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="58e84-115">-Name</span></span>
<span data-ttu-id="58e84-116">Bu cmdlet 'in kaldırdığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58e84-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58e84-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e84-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="58e84-118">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58e84-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="58e84-119">Bu nesne, kaldırılacak ağ güvenliği kuralı yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="58e84-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e84-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e84-120">CommonParameters</span></span>
<span data-ttu-id="58e84-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58e84-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e84-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e84-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e84-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58e84-123">INPUTS</span></span>

### <span data-ttu-id="58e84-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e84-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="58e84-125">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="58e84-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="58e84-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58e84-126">OUTPUTS</span></span>

### <span data-ttu-id="58e84-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e84-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="58e84-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58e84-128">NOTES</span></span>

## <span data-ttu-id="58e84-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58e84-129">RELATED LINKS</span></span>

[<span data-ttu-id="58e84-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58e84-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58e84-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58e84-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58e84-132">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58e84-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="58e84-133">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58e84-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58e84-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58e84-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


