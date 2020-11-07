---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935521"
---
# <span data-ttu-id="3e33f-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3e33f-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3e33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e33f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e33f-103">Ağ güvenlik grubunun ağ güvenlik kuralı yapılandırmasını alma.</span><span class="sxs-lookup"><span data-stu-id="3e33f-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3e33f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e33f-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e33f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e33f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e33f-106">**Get-AzNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubu için ağ güvenlik kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="3e33f-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="3e33f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e33f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e33f-108">1: ağ güvenlik kuralı yapılandırması alınıyor</span><span class="sxs-lookup"><span data-stu-id="3e33f-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="3e33f-109">Bu komut, "nsg1" kaynak grubundaki "Allowınternetoutbound" adlı Azure Network Security grubundan "RG1" adlı varsayılan kuralı alır</span><span class="sxs-lookup"><span data-stu-id="3e33f-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="3e33f-110">2: yalnızca adı kullanarak ağ güvenlik kuralı yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="3e33f-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="3e33f-111">Bu komut, "RG1" kaynak grubundaki "nsg1" adlı Azure Network Security grubundan "RDP-Rule" adlı Kullanıcı tanımlı kuralı alır</span><span class="sxs-lookup"><span data-stu-id="3e33f-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="3e33f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e33f-112">PARAMETERS</span></span>

### <span data-ttu-id="3e33f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e33f-113">-DefaultProfile</span></span>
<span data-ttu-id="3e33f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e33f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e33f-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="3e33f-115">-DefaultRules</span></span>
<span data-ttu-id="3e33f-116">Bu cmdlet 'in Kullanıcı tarafından oluşturulan bir kural yapılandırması mı yoksa varsayılan bir kural yapılandırması mı aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e33f-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="3e33f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e33f-117">-Name</span></span>
<span data-ttu-id="3e33f-118">Alınacak ağ güvenliği kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e33f-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="3e33f-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3e33f-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3e33f-120">Alınacak ağ güvenliği kuralı yapılandırmasını içeren bir **Networksecuritygroup** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e33f-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="3e33f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e33f-121">CommonParameters</span></span>
<span data-ttu-id="3e33f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e33f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e33f-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e33f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e33f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e33f-124">INPUTS</span></span>

### <span data-ttu-id="3e33f-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3e33f-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="3e33f-126">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3e33f-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="3e33f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e33f-127">OUTPUTS</span></span>

### <span data-ttu-id="3e33f-128">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="3e33f-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="3e33f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e33f-129">NOTES</span></span>

## <span data-ttu-id="3e33f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e33f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e33f-131">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3e33f-131">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3e33f-132">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3e33f-132">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3e33f-133">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3e33f-133">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3e33f-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3e33f-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


