---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 9b8da32a336b0320f8ca69b6f6e09d584315d0d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760290"
---
# <span data-ttu-id="69a45-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="69a45-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="69a45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a45-102">SYNOPSIS</span></span>
<span data-ttu-id="69a45-103">Genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69a45-103">Creates a public IP address.</span></span>

## <span data-ttu-id="69a45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69a45-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69a45-105">DESCRIPTION</span></span>
<span data-ttu-id="69a45-106">**New-Azpublicıpaddress** cmdlet 'i genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69a45-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="69a45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69a45-107">EXAMPLES</span></span>

### <span data-ttu-id="69a45-108">1: yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69a45-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="69a45-109">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="69a45-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="69a45-110">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="69a45-111">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="69a45-112">2: ters FQDN ile genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69a45-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="69a45-113">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69a45-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="69a45-114">-Smartfqdn parametresiyle, bu kaynağa tahsis edilen genel IP adresi için, komutta belirtilen $customFqdn işaret eden bir DNS PTR kaydı (ters arama) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="69a45-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="69a45-115">Önkoşul olarak, $customFqdn (say webapp.contoso.com), $dnsPrefix. $location. cloudapp.azure.com 'e işaret eden bir DNS CNAME kaydı (ileriye-arama) içermelidir.</span><span class="sxs-lookup"><span data-stu-id="69a45-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="69a45-116">3: ıptag ile yeni bir genel IP adresi oluşturun</span><span class="sxs-lookup"><span data-stu-id="69a45-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="69a45-117">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="69a45-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="69a45-118">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="69a45-119">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="69a45-120">Kaynak ile ilişkilendirilmiş etiketleri için ıptag kullanılır.</span><span class="sxs-lookup"><span data-stu-id="69a45-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="69a45-121">Iptag New-AzPublicIpTag kullanarak belirtilebilir ve-ıptags aracılığıyla giriş olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="69a45-122">4: önekten yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69a45-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="69a45-123">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69a45-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="69a45-124">$DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="69a45-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="69a45-125">Bu kaynağa, genel bir IP adresi belirtilen Publicıpprefix 'ten hemen tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="69a45-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="69a45-126">Bu seçenek yalnızca ' standart ' SKU ve ' static ' AllocationMethod ile desteklenir.</span><span class="sxs-lookup"><span data-stu-id="69a45-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="69a45-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69a45-127">PARAMETERS</span></span>

### <span data-ttu-id="69a45-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="69a45-128">-AllocationMethod</span></span>
<span data-ttu-id="69a45-129">Genel IP adresinin tahsis edilmesi yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="69a45-130">Bu parametre için kabul edilebilir değerler: statik veya dinamik.</span><span class="sxs-lookup"><span data-stu-id="69a45-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="69a45-131">-AsJob</span></span>
<span data-ttu-id="69a45-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="69a45-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69a45-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a45-133">-DefaultProfile</span></span>
<span data-ttu-id="69a45-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69a45-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69a45-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="69a45-135">-DomainNameLabel</span></span>
<span data-ttu-id="69a45-136">Genel bir IP adresi için göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-136">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-137">-Force</span><span class="sxs-lookup"><span data-stu-id="69a45-137">-Force</span></span>
<span data-ttu-id="69a45-138">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="69a45-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69a45-139">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="69a45-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="69a45-140">Bekleme süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-140">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="69a45-141">-IpAddressVersion</span></span>
<span data-ttu-id="69a45-142">IP adresinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-143">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="69a45-143">-IpTag</span></span>
<span data-ttu-id="69a45-144">Iptag listesi.</span><span class="sxs-lookup"><span data-stu-id="69a45-144">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="69a45-145">-Location</span></span>
<span data-ttu-id="69a45-146">Genel IP adresi oluşturacağınız bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-146">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="69a45-147">-Name</span></span>
<span data-ttu-id="69a45-148">Bu cmdlet 'in oluşturduğu ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-149">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="69a45-149">-PublicIpPrefix</span></span>
<span data-ttu-id="69a45-150">Genel IP adresi ayrılacak PSPublicIpPrefix öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a45-151">-ResourceGroupName</span></span>
<span data-ttu-id="69a45-152">Genel IP adresi oluşturacağınız kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="69a45-153">-Smarfqdn</span><span class="sxs-lookup"><span data-stu-id="69a45-153">-ReverseFqdn</span></span>
<span data-ttu-id="69a45-154">Geriye doğru tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a45-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="69a45-155">-Sku</span></span>
<span data-ttu-id="69a45-156">Genel IP SKU adı.</span><span class="sxs-lookup"><span data-stu-id="69a45-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="69a45-157">-Tag</span></span>
<span data-ttu-id="69a45-158">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="69a45-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="69a45-159">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="69a45-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="69a45-160">-Bölge</span><span class="sxs-lookup"><span data-stu-id="69a45-160">-Zone</span></span>
<span data-ttu-id="69a45-161">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="69a45-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a45-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="69a45-162">-Confirm</span></span>
<span data-ttu-id="69a45-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69a45-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a45-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a45-164">-WhatIf</span></span>
<span data-ttu-id="69a45-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69a45-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a45-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69a45-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a45-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a45-167">CommonParameters</span></span>
<span data-ttu-id="69a45-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69a45-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a45-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a45-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a45-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69a45-170">INPUTS</span></span>

### <span data-ttu-id="69a45-171">System. String</span><span class="sxs-lookup"><span data-stu-id="69a45-171">System.String</span></span>

### <span data-ttu-id="69a45-172">Microsoft. Azure. Commands. Network. model. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="69a45-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="69a45-173">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="69a45-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="69a45-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="69a45-174">System.Int32</span></span>

### <span data-ttu-id="69a45-175">System. String []</span><span class="sxs-lookup"><span data-stu-id="69a45-175">System.String[]</span></span>

### <span data-ttu-id="69a45-176">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="69a45-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69a45-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69a45-177">OUTPUTS</span></span>

### <span data-ttu-id="69a45-178">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="69a45-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="69a45-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69a45-179">NOTES</span></span>

## <span data-ttu-id="69a45-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69a45-180">RELATED LINKS</span></span>

[<span data-ttu-id="69a45-181">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="69a45-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="69a45-182">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="69a45-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="69a45-183">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="69a45-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
