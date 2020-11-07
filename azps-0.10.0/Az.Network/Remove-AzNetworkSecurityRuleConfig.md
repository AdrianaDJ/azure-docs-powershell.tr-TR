---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 8a2851f34cfbeb9fec72830334c52a9b4a83d064
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935281"
---
# <span data-ttu-id="ed2d2-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed2d2-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ed2d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2d2-103">Ağ güvenlik grubundan bir ağ güvenliği kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="ed2d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed2d2-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed2d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed2d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2d2-106">**Remove-AzNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubundan ağ güvenliği kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="ed2d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed2d2-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2d2-108">Örnek 1: ağ güvenlik kuralı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed2d2-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="ed2d2-109">İlk komut, RDP kuralı adlı bir ağ güvenlik kuralı yapılandırması oluşturur ve $rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="ed2d2-110">İkinci komut $rule 1 ' deki kuralı kullanarak bir ağ güvenlik grubu oluşturur ve ardından ağ güvenlik grubunu $nsg değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="ed2d2-111">Üçüncü komut, $nsg 'daki ağ güvenliği grubundan RDP-kuralı adlı ağ güvenlik kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="ed2d2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed2d2-112">PARAMETERS</span></span>

### <span data-ttu-id="ed2d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2d2-113">-DefaultProfile</span></span>
<span data-ttu-id="ed2d2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2d2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed2d2-115">-Name</span></span>
<span data-ttu-id="ed2d2-116">Bu cmdlet 'in kaldırdığı ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ed2d2-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed2d2-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ed2d2-118">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ed2d2-119">Bu nesne, kaldırılacak ağ güvenliği kuralı yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="ed2d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2d2-120">CommonParameters</span></span>
<span data-ttu-id="ed2d2-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed2d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2d2-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2d2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2d2-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed2d2-123">INPUTS</span></span>

### <span data-ttu-id="ed2d2-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed2d2-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="ed2d2-125">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ed2d2-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="ed2d2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed2d2-126">OUTPUTS</span></span>

### <span data-ttu-id="ed2d2-127">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed2d2-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ed2d2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed2d2-128">NOTES</span></span>

## <span data-ttu-id="ed2d2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed2d2-129">RELATED LINKS</span></span>

[<span data-ttu-id="ed2d2-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed2d2-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed2d2-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed2d2-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed2d2-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ed2d2-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ed2d2-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed2d2-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ed2d2-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed2d2-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


