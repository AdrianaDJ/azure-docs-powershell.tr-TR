---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762702"
---
# <span data-ttu-id="8b2c0-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c0-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="8b2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2c0-103">Ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b2c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b2c0-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b2c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2c0-106">**New-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="8b2c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b2c0-107">EXAMPLES</span></span>

### <span data-ttu-id="8b2c0-108">1: yeni ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b2c0-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="8b2c0-109">Bu komut, "RG1" kaynak grubunda "westus" adlı yeni bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="8b2c0-110">2: ayrıntılı ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b2c0-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="8b2c0-111">Adım: 1 Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="8b2c0-112">Adım: 2 Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="8b2c0-113">Adım: 3 yukarıda oluşturulan kuralları yeni bir NSG-ön uç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="8b2c0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b2c0-114">PARAMETERS</span></span>

### <span data-ttu-id="8b2c0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b2c0-115">-Force</span></span>
<span data-ttu-id="8b2c0-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b2c0-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b2c0-117">-Location</span></span>
<span data-ttu-id="8b2c0-118">Ağ güvenlik grubu oluşturulacak bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-118">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b2c0-119">-Name</span></span>
<span data-ttu-id="8b2c0-120">Oluşturulacak ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-120">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b2c0-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8b2c0-123">Bu cmdlet, bu parametrenin belirttiği kaynak grubunda bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="8b2c0-124">-SecurityRules</span></span>
<span data-ttu-id="8b2c0-125">Ağ güvenlik grubunda oluşturulacak ağ güvenliği kuralı nesnelerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8b2c0-126">-Tag</span></span>
<span data-ttu-id="8b2c0-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8b2c0-128">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8b2c0-128">For example:</span></span>

<span data-ttu-id="8b2c0-129">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8b2c0-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b2c0-130">-Confirm</span></span>
<span data-ttu-id="8b2c0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2c0-132">-WhatIf</span></span>
<span data-ttu-id="8b2c0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2c0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b2c0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2c0-135">-DefaultProfile</span></span>
<span data-ttu-id="8b2c0-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b2c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2c0-137">CommonParameters</span></span>
<span data-ttu-id="8b2c0-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2c0-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b2c0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2c0-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b2c0-140">INPUTS</span></span>

## <span data-ttu-id="8b2c0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b2c0-141">OUTPUTS</span></span>

### <span data-ttu-id="8b2c0-142">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c0-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8b2c0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b2c0-143">NOTES</span></span>

## <span data-ttu-id="8b2c0-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b2c0-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b2c0-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c0-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="8b2c0-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c0-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="8b2c0-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b2c0-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
