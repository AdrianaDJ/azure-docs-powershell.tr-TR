---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 3bfed7f4c980ab246f4e38d500860ccd4e2ef09f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323761"
---
# <span data-ttu-id="40729-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="40729-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="40729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40729-102">SYNOPSIS</span></span>
<span data-ttu-id="40729-103">Genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40729-103">Creates a public IP address.</span></span>

## <span data-ttu-id="40729-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40729-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40729-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40729-105">DESCRIPTION</span></span>
<span data-ttu-id="40729-106">**New-Azpublicıpaddress** cmdlet 'i genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40729-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="40729-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40729-107">EXAMPLES</span></span>

### <span data-ttu-id="40729-108">Örnek 1: yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="40729-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="40729-109">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="40729-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="40729-110">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="40729-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="40729-111">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="40729-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="40729-112">Örnek 2: ters FQDN ile genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="40729-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="40729-113">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40729-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="40729-114">-Smartfqdn parametresiyle, bu kaynağa tahsis edilen genel IP adresi için, komutta belirtilen $customFqdn işaret eden bir DNS PTR kaydı (ters arama) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="40729-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="40729-115">Önkoşul olarak, $customFqdn (say webapp.contoso.com), $dnsPrefix. $location. cloudapp.azure.com 'e işaret eden bir DNS CNAME kaydı (ileriye-arama) içermelidir.</span><span class="sxs-lookup"><span data-stu-id="40729-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="40729-116">Örnek 3: ıptag ile yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="40729-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="40729-117">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="40729-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="40729-118">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="40729-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="40729-119">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="40729-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="40729-120">Kaynak ile ilişkilendirilmiş etiketleri için ıptag kullanılır.</span><span class="sxs-lookup"><span data-stu-id="40729-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="40729-121">Iptag New-AzPublicIpTag kullanarak belirtilebilir ve-ıptags aracılığıyla giriş olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="40729-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="40729-122">Örnek 4: önekten yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="40729-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="40729-123">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40729-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="40729-124">$DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="40729-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="40729-125">Bu kaynağa, genel bir IP adresi belirtilen Publicıpprefix 'ten hemen tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="40729-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="40729-126">Bu seçenek yalnızca ' standart ' SKU ve ' static ' AllocationMethod ile desteklenir.</span><span class="sxs-lookup"><span data-stu-id="40729-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="40729-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40729-127">PARAMETERS</span></span>

### <span data-ttu-id="40729-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="40729-128">-AllocationMethod</span></span>
<span data-ttu-id="40729-129">Genel IP adresinin tahsis edilmesi yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="40729-130">Bu parametre için kabul edilebilir değerler: statik veya dinamik.</span><span class="sxs-lookup"><span data-stu-id="40729-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="40729-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="40729-131">-AsJob</span></span>
<span data-ttu-id="40729-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="40729-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40729-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40729-133">-DefaultProfile</span></span>
<span data-ttu-id="40729-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40729-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40729-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="40729-135">-DomainNameLabel</span></span>
<span data-ttu-id="40729-136">Genel bir IP adresi için göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="40729-137">-Force</span><span class="sxs-lookup"><span data-stu-id="40729-137">-Force</span></span>
<span data-ttu-id="40729-138">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="40729-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40729-139">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="40729-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="40729-140">Bekleme süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="40729-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="40729-141">-IpAddressVersion</span></span>
<span data-ttu-id="40729-142">IP adresinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="40729-143">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="40729-143">-IpTag</span></span>
<span data-ttu-id="40729-144">Iptag listesi.</span><span class="sxs-lookup"><span data-stu-id="40729-144">IpTag List.</span></span>

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

### <span data-ttu-id="40729-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="40729-145">-Location</span></span>
<span data-ttu-id="40729-146">Genel IP adresi oluşturacağınız bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="40729-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="40729-147">-Name</span></span>
<span data-ttu-id="40729-148">Bu cmdlet 'in oluşturduğu ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="40729-149">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="40729-149">-PublicIpPrefix</span></span>
<span data-ttu-id="40729-150">Genel IP adresi ayrılacak PSPublicIpPrefix öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="40729-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40729-151">-ResourceGroupName</span></span>
<span data-ttu-id="40729-152">Genel IP adresi oluşturacağınız kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="40729-153">-Smarfqdn</span><span class="sxs-lookup"><span data-stu-id="40729-153">-ReverseFqdn</span></span>
<span data-ttu-id="40729-154">Geriye doğru tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="40729-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="40729-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="40729-155">-Sku</span></span>
<span data-ttu-id="40729-156">Genel IP SKU adı.</span><span class="sxs-lookup"><span data-stu-id="40729-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="40729-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="40729-157">-Tag</span></span>
<span data-ttu-id="40729-158">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="40729-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40729-159">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="40729-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="40729-160">-Bölge</span><span class="sxs-lookup"><span data-stu-id="40729-160">-Zone</span></span>
<span data-ttu-id="40729-161">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="40729-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="40729-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="40729-162">-Confirm</span></span>
<span data-ttu-id="40729-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40729-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40729-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40729-164">-WhatIf</span></span>
<span data-ttu-id="40729-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40729-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40729-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40729-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40729-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40729-167">CommonParameters</span></span>
<span data-ttu-id="40729-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40729-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40729-169">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40729-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40729-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40729-170">INPUTS</span></span>

### <span data-ttu-id="40729-171">System. String</span><span class="sxs-lookup"><span data-stu-id="40729-171">System.String</span></span>

### <span data-ttu-id="40729-172">Microsoft. Azure. Commands. Network. model. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="40729-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="40729-173">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="40729-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="40729-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="40729-174">System.Int32</span></span>

### <span data-ttu-id="40729-175">System. String []</span><span class="sxs-lookup"><span data-stu-id="40729-175">System.String[]</span></span>

### <span data-ttu-id="40729-176">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="40729-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="40729-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40729-177">OUTPUTS</span></span>

### <span data-ttu-id="40729-178">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="40729-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="40729-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40729-179">NOTES</span></span>

## <span data-ttu-id="40729-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40729-180">RELATED LINKS</span></span>

[<span data-ttu-id="40729-181">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="40729-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="40729-182">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="40729-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="40729-183">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="40729-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
