---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1ad99522e93587b2f335ae35478aedbc6cc36e88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097538"
---
# <span data-ttu-id="ca8fa-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca8fa-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="ca8fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8fa-103">Ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-103">Creates a network security group.</span></span>

## <span data-ttu-id="ca8fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca8fa-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca8fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8fa-106">**New-AzNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="ca8fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca8fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8fa-108">1: yeni ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca8fa-108">1: Create a new network security group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="ca8fa-109">Bu komut, "RG1" kaynak grubunda "westus" adlı yeni bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="ca8fa-110">2: ayrıntılı ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca8fa-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="ca8fa-111">Adım: 1 Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="ca8fa-112">Adım: 2 Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="ca8fa-113">Adım: 3 yukarıda oluşturulan kuralları yeni bir NSG-ön uç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="ca8fa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca8fa-114">PARAMETERS</span></span>

### <span data-ttu-id="ca8fa-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ca8fa-115">-AsJob</span></span>
<span data-ttu-id="ca8fa-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ca8fa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca8fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8fa-117">-DefaultProfile</span></span>
<span data-ttu-id="ca8fa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8fa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ca8fa-119">-Force</span></span>
<span data-ttu-id="ca8fa-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca8fa-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca8fa-121">-Location</span></span>
<span data-ttu-id="ca8fa-122">Ağ güvenlik grubu oluşturulacak bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="ca8fa-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca8fa-123">-Name</span></span>
<span data-ttu-id="ca8fa-124">Oluşturulacak ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="ca8fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca8fa-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ca8fa-127">Bu cmdlet, bu parametrenin belirttiği kaynak grubunda bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca8fa-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="ca8fa-128">-SecurityRules</span></span>
<span data-ttu-id="ca8fa-129">Ağ güvenlik grubunda oluşturulacak ağ güvenliği kuralı nesnelerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8fa-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ca8fa-130">-Tag</span></span>
<span data-ttu-id="ca8fa-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca8fa-132">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ca8fa-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ca8fa-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca8fa-133">-Confirm</span></span>
<span data-ttu-id="ca8fa-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8fa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8fa-135">-WhatIf</span></span>
<span data-ttu-id="ca8fa-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8fa-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8fa-138">CommonParameters</span></span>
<span data-ttu-id="ca8fa-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca8fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8fa-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8fa-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8fa-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca8fa-141">INPUTS</span></span>

### <span data-ttu-id="ca8fa-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8fa-142">System.String</span></span>

### <span data-ttu-id="ca8fa-143">Microsoft. Azure. Commands. Network. model. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="ca8fa-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="ca8fa-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca8fa-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca8fa-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca8fa-145">OUTPUTS</span></span>

### <span data-ttu-id="ca8fa-146">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca8fa-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ca8fa-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca8fa-147">NOTES</span></span>

## <span data-ttu-id="ca8fa-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca8fa-148">RELATED LINKS</span></span>

[<span data-ttu-id="ca8fa-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca8fa-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ca8fa-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca8fa-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ca8fa-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca8fa-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
