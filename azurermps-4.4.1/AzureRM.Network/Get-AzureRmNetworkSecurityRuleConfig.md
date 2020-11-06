---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 903738f1cb2e816ce18c9e5e3c9b01cf3d4baa9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594627"
---
# <span data-ttu-id="7f4a2-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f4a2-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7f4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4a2-103">Ağ güvenlik grubunun ağ güvenlik kuralı yapılandırmasını alma.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f4a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f4a2-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f4a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="7f4a2-106">**Get-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubu için ağ güvenlik kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="7f4a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f4a2-107">EXAMPLES</span></span>

### <span data-ttu-id="7f4a2-108">1: ağ güvenlik kuralı yapılandırması alınıyor</span><span class="sxs-lookup"><span data-stu-id="7f4a2-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="7f4a2-109">Bu komut, "nsg1" kaynak grubundaki "Allowınternetoutbound" adlı Azure Network Security grubundan "RG1" adlı varsayılan kuralı alır</span><span class="sxs-lookup"><span data-stu-id="7f4a2-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="7f4a2-110">2: yalnızca adı kullanarak ağ güvenlik kuralı yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="7f4a2-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="7f4a2-111">Bu komut, "RG1" kaynak grubundaki "nsg1" adlı Azure Network Security grubundan "RDP-Rule" adlı Kullanıcı tanımlı kuralı alır</span><span class="sxs-lookup"><span data-stu-id="7f4a2-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="7f4a2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f4a2-112">PARAMETERS</span></span>

### <span data-ttu-id="7f4a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4a2-113">-DefaultProfile</span></span>
<span data-ttu-id="7f4a2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4a2-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="7f4a2-115">-DefaultRules</span></span>
<span data-ttu-id="7f4a2-116">Bu cmdlet 'in Kullanıcı tarafından oluşturulan bir kural yapılandırması mı yoksa varsayılan bir kural yapılandırması mı aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="7f4a2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f4a2-117">-Name</span></span>
<span data-ttu-id="7f4a2-118">Alınacak ağ güvenliği kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4a2-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f4a2-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7f4a2-120">Alınacak ağ güvenliği kuralı yapılandırmasını içeren bir **Networksecuritygroup** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4a2-121">CommonParameters</span></span>
<span data-ttu-id="7f4a2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f4a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4a2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f4a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4a2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f4a2-124">INPUTS</span></span>

### <span data-ttu-id="7f4a2-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f4a2-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="7f4a2-126">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7f4a2-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="7f4a2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f4a2-127">OUTPUTS</span></span>

### <span data-ttu-id="7f4a2-128">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7f4a2-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="7f4a2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f4a2-129">NOTES</span></span>

## <span data-ttu-id="7f4a2-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f4a2-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f4a2-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f4a2-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f4a2-132">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f4a2-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f4a2-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f4a2-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f4a2-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f4a2-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


