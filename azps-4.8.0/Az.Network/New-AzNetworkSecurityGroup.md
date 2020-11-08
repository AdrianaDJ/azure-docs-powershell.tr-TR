---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268481"
---
# <span data-ttu-id="e1af0-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1af0-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e1af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1af0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1af0-103">Ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1af0-103">Creates a network security group.</span></span>

## <span data-ttu-id="e1af0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1af0-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1af0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1af0-105">DESCRIPTION</span></span>
<span data-ttu-id="e1af0-106">**New-AzNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1af0-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="e1af0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1af0-107">EXAMPLES</span></span>

### <span data-ttu-id="e1af0-108">Örnek 1: yeni bir ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e1af0-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="e1af0-109">Bu komut, "RG1" kaynak grubunda "westus" adlı yeni bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1af0-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="e1af0-110">Örnek 2: ayrıntılı ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e1af0-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="e1af0-111">Adım: 1 Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1af0-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="e1af0-112">Adım: 2 Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1af0-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="e1af0-113">Adım: 3 yukarıda oluşturulan kuralları yeni bir NSG-ön uç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e1af0-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="e1af0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1af0-114">PARAMETERS</span></span>

### <span data-ttu-id="e1af0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="e1af0-115">-AsJob</span></span>
<span data-ttu-id="e1af0-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e1af0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1af0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1af0-117">-DefaultProfile</span></span>
<span data-ttu-id="e1af0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1af0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1af0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e1af0-119">-Force</span></span>
<span data-ttu-id="e1af0-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e1af0-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1af0-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="e1af0-121">-Location</span></span>
<span data-ttu-id="e1af0-122">Ağ güvenlik grubu oluşturulacak bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1af0-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="e1af0-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1af0-123">-Name</span></span>
<span data-ttu-id="e1af0-124">Oluşturulacak ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1af0-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="e1af0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1af0-125">-ResourceGroupName</span></span>
<span data-ttu-id="e1af0-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1af0-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e1af0-127">Bu cmdlet, bu parametrenin belirttiği kaynak grubunda bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1af0-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1af0-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="e1af0-128">-SecurityRules</span></span>
<span data-ttu-id="e1af0-129">Ağ güvenlik grubunda oluşturulacak ağ güvenliği kuralı nesnelerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1af0-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="e1af0-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e1af0-130">-Tag</span></span>
<span data-ttu-id="e1af0-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e1af0-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e1af0-132">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e1af0-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e1af0-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1af0-133">-Confirm</span></span>
<span data-ttu-id="e1af0-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1af0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1af0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1af0-135">-WhatIf</span></span>
<span data-ttu-id="e1af0-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1af0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1af0-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1af0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1af0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1af0-138">CommonParameters</span></span>
<span data-ttu-id="e1af0-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1af0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1af0-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1af0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1af0-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1af0-141">INPUTS</span></span>

### <span data-ttu-id="e1af0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e1af0-142">System.String</span></span>

### <span data-ttu-id="e1af0-143">Microsoft. Azure. Commands. Network. model. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="e1af0-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="e1af0-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1af0-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1af0-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1af0-145">OUTPUTS</span></span>

### <span data-ttu-id="e1af0-146">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1af0-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e1af0-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1af0-147">NOTES</span></span>

## <span data-ttu-id="e1af0-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1af0-148">RELATED LINKS</span></span>

[<span data-ttu-id="e1af0-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1af0-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e1af0-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1af0-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e1af0-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e1af0-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
