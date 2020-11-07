---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: f62b7bb2b338247305c53199b7f1e7087f195ffd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918251"
---
# <span data-ttu-id="271b4-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="271b4-101">New-AzNatGateway</span></span>

## <span data-ttu-id="271b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="271b4-102">SYNOPSIS</span></span>
<span data-ttu-id="271b4-103">Ortak IP adresi/genel IP öneki, ıdzamanzamansayısı ve SKU ile yeni NAT ağ geçidi kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="271b4-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="271b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="271b4-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="271b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="271b4-105">DESCRIPTION</span></span>
<span data-ttu-id="271b4-106">**Yeni-AzNatGateway** cmdlet 'ı NAT ağ geçidi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="271b4-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="271b4-107">Natgateway aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="271b4-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="271b4-108">Ortak IP adresi ve/veya genel IP öneki</span><span class="sxs-lookup"><span data-stu-id="271b4-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="271b4-109">Idfaizsüresi</span><span class="sxs-lookup"><span data-stu-id="271b4-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="271b4-110">'Sunda</span><span class="sxs-lookup"><span data-stu-id="271b4-110">Sku</span></span>
- <span data-ttu-id="271b4-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271b4-111">ResourceGroupName</span></span>
- <span data-ttu-id="271b4-112">Kaynak</span><span class="sxs-lookup"><span data-stu-id="271b4-112">ResourceName</span></span>
- <span data-ttu-id="271b4-113">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="271b4-113">Location</span></span>

## <span data-ttu-id="271b4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="271b4-114">EXAMPLES</span></span>

### <span data-ttu-id="271b4-115">Örnek 1: genel IP adresiyle NAT ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="271b4-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="271b4-116">Örnek 2: genel IP önekiyle NAT ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="271b4-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="271b4-117">Örnek 3: kullanılabilirlik bölgesi 1 ' de genel IP adresiyle NAT ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="271b4-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="271b4-118">İlk komut standart genel IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="271b4-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="271b4-119">İkinci komut, kullanılabilirlik bölgesi 1 ' de genel IP adresiyle NAT ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="271b4-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="271b4-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="271b4-120">PARAMETERS</span></span>

### <span data-ttu-id="271b4-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="271b4-121">-AsJob</span></span>
<span data-ttu-id="271b4-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="271b4-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="271b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271b4-123">-DefaultProfile</span></span>
<span data-ttu-id="271b4-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="271b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="271b4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="271b4-125">-Force</span></span>
<span data-ttu-id="271b4-126">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="271b4-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="271b4-127">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="271b4-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="271b4-128">NAT ağ geçidinin Boşta durma süresi.</span><span class="sxs-lookup"><span data-stu-id="271b4-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="271b4-129">-Location</span></span>
<span data-ttu-id="271b4-130">Konum.</span><span class="sxs-lookup"><span data-stu-id="271b4-130">The location.</span></span>

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

### <span data-ttu-id="271b4-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="271b4-131">-Name</span></span>
<span data-ttu-id="271b4-132">NAT ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="271b4-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-133">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="271b4-133">-PublicIpAddress</span></span>
<span data-ttu-id="271b4-134">NAT ağ geçidi kaynağıyla ilişkili ortak IP adresleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="271b4-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-135">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="271b4-135">-PublicIpPrefix</span></span>
<span data-ttu-id="271b4-136">NAT ağ geçidi kaynağıyla ilişkili genel IP önekleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="271b4-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271b4-137">-ResourceGroupName</span></span>
<span data-ttu-id="271b4-138">NAT ağ geçidinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="271b4-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="271b4-139">-Sku</span></span>
<span data-ttu-id="271b4-140">NAT ağ geçidi SKU 'SU adı.</span><span class="sxs-lookup"><span data-stu-id="271b4-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="271b4-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="271b4-141">-Tag</span></span>
<span data-ttu-id="271b4-142">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="271b4-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-143">-Bölge</span><span class="sxs-lookup"><span data-stu-id="271b4-143">-Zone</span></span>
<span data-ttu-id="271b4-144">NAT ağ geçidinin dağıtılması gereken bölgeyi belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="271b4-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="271b4-145">-Confirm</span></span>
<span data-ttu-id="271b4-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="271b4-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271b4-147">-WhatIf</span></span>
<span data-ttu-id="271b4-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="271b4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="271b4-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="271b4-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271b4-150">CommonParameters</span></span>
<span data-ttu-id="271b4-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="271b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271b4-152">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="271b4-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271b4-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="271b4-153">INPUTS</span></span>

### <span data-ttu-id="271b4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="271b4-154">System.String</span></span>

### <span data-ttu-id="271b4-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="271b4-155">System.Int32</span></span>

### <span data-ttu-id="271b4-156">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="271b4-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="271b4-157">Microsoft. Azure. Commands. Network. model. Psresourceıd []</span><span class="sxs-lookup"><span data-stu-id="271b4-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="271b4-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="271b4-158">OUTPUTS</span></span>

### <span data-ttu-id="271b4-159">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="271b4-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="271b4-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="271b4-160">NOTES</span></span>

## <span data-ttu-id="271b4-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="271b4-161">RELATED LINKS</span></span>
