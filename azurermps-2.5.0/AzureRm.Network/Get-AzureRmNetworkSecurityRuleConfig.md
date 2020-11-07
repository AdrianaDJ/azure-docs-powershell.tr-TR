---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940074"
---
# <span data-ttu-id="41caf-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41caf-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="41caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41caf-102">SYNOPSIS</span></span>
<span data-ttu-id="41caf-103">Ağ güvenlik grubunun ağ güvenlik kuralı yapılandırmasını alma.</span><span class="sxs-lookup"><span data-stu-id="41caf-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41caf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41caf-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41caf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41caf-105">DESCRIPTION</span></span>
<span data-ttu-id="41caf-106">**Get-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubu için ağ güvenlik kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="41caf-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="41caf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41caf-107">EXAMPLES</span></span>

### <span data-ttu-id="41caf-108">1: ağ güvenlik kuralı yapılandırması alınıyor</span><span class="sxs-lookup"><span data-stu-id="41caf-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="41caf-109">Bu komut, "nsg1" kaynak grubundaki "Allowınternetoutbound" adlı Azure Network Security grubundan "RG1" adlı varsayılan kuralı alır</span><span class="sxs-lookup"><span data-stu-id="41caf-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="41caf-110">2: yalnızca adı kullanarak ağ güvenlik kuralı yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="41caf-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="41caf-111">Bu komut, "RG1" kaynak grubundaki "nsg1" adlı Azure Network Security grubundan "RDP-Rule" adlı Kullanıcı tanımlı kuralı alır</span><span class="sxs-lookup"><span data-stu-id="41caf-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="41caf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41caf-112">PARAMETERS</span></span>

### <span data-ttu-id="41caf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41caf-113">-DefaultProfile</span></span>
<span data-ttu-id="41caf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41caf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41caf-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="41caf-115">-DefaultRules</span></span>
<span data-ttu-id="41caf-116">Bu cmdlet 'in Kullanıcı tarafından oluşturulan bir kural yapılandırması mı yoksa varsayılan bir kural yapılandırması mı aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41caf-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="41caf-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="41caf-117">-Name</span></span>
<span data-ttu-id="41caf-118">Alınacak ağ güvenliği kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41caf-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="41caf-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41caf-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="41caf-120">Alınacak ağ güvenliği kuralı yapılandırmasını içeren bir **Networksecuritygroup** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="41caf-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="41caf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41caf-121">CommonParameters</span></span>
<span data-ttu-id="41caf-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41caf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41caf-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41caf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41caf-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41caf-124">INPUTS</span></span>

### <span data-ttu-id="41caf-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="41caf-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="41caf-126">' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="41caf-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="41caf-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41caf-127">OUTPUTS</span></span>

### <span data-ttu-id="41caf-128">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="41caf-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="41caf-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41caf-129">NOTES</span></span>

## <span data-ttu-id="41caf-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41caf-130">RELATED LINKS</span></span>

[<span data-ttu-id="41caf-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41caf-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41caf-132">Yeni-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41caf-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41caf-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41caf-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="41caf-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41caf-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


