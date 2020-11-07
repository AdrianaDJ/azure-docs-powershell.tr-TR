---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: a4d8386cdcdee8b67bea746e40a9035acf3bcce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765092"
---
# <span data-ttu-id="f4130-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4130-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="f4130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4130-102">SYNOPSIS</span></span>
<span data-ttu-id="f4130-103">Ağ güvenlik grubunun ağ güvenlik kuralı yapılandırmasını alma.</span><span class="sxs-lookup"><span data-stu-id="f4130-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4130-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4130-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4130-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4130-105">DESCRIPTION</span></span>
<span data-ttu-id="f4130-106">**Get-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubu için ağ güvenlik kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4130-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="f4130-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4130-107">EXAMPLES</span></span>

### <span data-ttu-id="f4130-108">1: ağ güvenlik kuralı yapılandırması alınıyor</span><span class="sxs-lookup"><span data-stu-id="f4130-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="f4130-109">Bu komut, "nsg1" kaynak grubundaki "Allowınternetoutbound" adlı Azure Network Security grubundan "RG1" adlı varsayılan kuralı alır</span><span class="sxs-lookup"><span data-stu-id="f4130-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="f4130-110">2: yalnızca adı kullanarak ağ güvenlik kuralı yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="f4130-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="f4130-111">Bu komut, "RG1" kaynak grubundaki "nsg1" adlı Azure Network Security grubundan "RDP-Rule" adlı Kullanıcı tanımlı kuralı alır</span><span class="sxs-lookup"><span data-stu-id="f4130-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="f4130-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4130-112">PARAMETERS</span></span>

### <span data-ttu-id="f4130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4130-113">-DefaultProfile</span></span>
<span data-ttu-id="f4130-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4130-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4130-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="f4130-115">-DefaultRules</span></span>
<span data-ttu-id="f4130-116">Bu cmdlet 'in Kullanıcı tarafından oluşturulan bir kural yapılandırması mı yoksa varsayılan bir kural yapılandırması mı aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4130-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="f4130-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4130-117">-Name</span></span>
<span data-ttu-id="f4130-118">Alınacak ağ güvenliği kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4130-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="f4130-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4130-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f4130-120">Alınacak ağ güvenliği kuralı yapılandırmasını içeren bir **Networksecuritygroup** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4130-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="f4130-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4130-121">CommonParameters</span></span>
<span data-ttu-id="f4130-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4130-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4130-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4130-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4130-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4130-124">INPUTS</span></span>

### <span data-ttu-id="f4130-125">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f4130-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="f4130-126">Parametreler: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4130-126">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="f4130-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4130-127">OUTPUTS</span></span>

### <span data-ttu-id="f4130-128">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="f4130-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="f4130-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4130-129">NOTES</span></span>

## <span data-ttu-id="f4130-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4130-130">RELATED LINKS</span></span>

[<span data-ttu-id="f4130-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4130-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f4130-132">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4130-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f4130-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4130-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="f4130-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4130-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


