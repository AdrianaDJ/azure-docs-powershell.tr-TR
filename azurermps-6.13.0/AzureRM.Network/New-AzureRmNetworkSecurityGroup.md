---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 1ffcad92a50cc332fdcab71337112b8d0c436388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591350"
---
# <span data-ttu-id="da597-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da597-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="da597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da597-102">SYNOPSIS</span></span>
<span data-ttu-id="da597-103">Ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da597-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da597-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da597-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da597-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da597-105">DESCRIPTION</span></span>
<span data-ttu-id="da597-106">**New-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da597-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="da597-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da597-107">EXAMPLES</span></span>

### <span data-ttu-id="da597-108">1: yeni ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="da597-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="da597-109">Bu komut, "RG1" kaynak grubunda "westus" adlı yeni bir Azure ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da597-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="da597-110">2: ayrıntılı ağ güvenlik grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="da597-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="da597-111">Adım: 1 Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="da597-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="da597-112">Adım: 2 Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="da597-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="da597-113">Adım: 3 yukarıda oluşturulan kuralları yeni bir NSG-ön uç olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da597-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="da597-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da597-114">PARAMETERS</span></span>

### <span data-ttu-id="da597-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="da597-115">-AsJob</span></span>
<span data-ttu-id="da597-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="da597-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da597-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da597-117">-DefaultProfile</span></span>
<span data-ttu-id="da597-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da597-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da597-119">-Force</span><span class="sxs-lookup"><span data-stu-id="da597-119">-Force</span></span>
<span data-ttu-id="da597-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="da597-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da597-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="da597-121">-Location</span></span>
<span data-ttu-id="da597-122">Ağ güvenlik grubu oluşturulacak bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="da597-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="da597-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="da597-123">-Name</span></span>
<span data-ttu-id="da597-124">Oluşturulacak ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da597-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="da597-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da597-125">-ResourceGroupName</span></span>
<span data-ttu-id="da597-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da597-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="da597-127">Bu cmdlet, bu parametrenin belirttiği kaynak grubunda bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da597-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da597-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="da597-128">-SecurityRules</span></span>
<span data-ttu-id="da597-129">Ağ güvenlik grubunda oluşturulacak ağ güvenliği kuralı nesnelerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da597-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="da597-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="da597-130">-Tag</span></span>
<span data-ttu-id="da597-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="da597-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da597-132">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="da597-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da597-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="da597-133">-Confirm</span></span>
<span data-ttu-id="da597-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da597-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da597-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da597-135">-WhatIf</span></span>
<span data-ttu-id="da597-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da597-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da597-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da597-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da597-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da597-138">CommonParameters</span></span>
<span data-ttu-id="da597-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da597-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da597-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da597-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da597-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da597-141">INPUTS</span></span>

### <span data-ttu-id="da597-142">System. String</span><span class="sxs-lookup"><span data-stu-id="da597-142">System.String</span></span>

### <span data-ttu-id="da597-143">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSSecurityRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da597-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSecurityRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="da597-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da597-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da597-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da597-145">OUTPUTS</span></span>

### <span data-ttu-id="da597-146">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da597-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="da597-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da597-147">NOTES</span></span>

## <span data-ttu-id="da597-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da597-148">RELATED LINKS</span></span>

[<span data-ttu-id="da597-149">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da597-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="da597-150">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da597-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="da597-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="da597-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
