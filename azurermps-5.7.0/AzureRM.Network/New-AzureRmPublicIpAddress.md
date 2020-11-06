---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594063"
---
# <span data-ttu-id="9bdc5-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9bdc5-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="9bdc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdc5-103">Genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bdc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bdc5-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bdc5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bdc5-105">DESCRIPTION</span></span>
<span data-ttu-id="9bdc5-106">**Yeni-Azurermpublicıpaddress** cmdlet 'i genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="9bdc5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bdc5-107">EXAMPLES</span></span>

### <span data-ttu-id="9bdc5-108">1: yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9bdc5-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="9bdc5-109">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="9bdc5-110">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="9bdc5-111">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="9bdc5-112">2: ters FQDN ile genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9bdc5-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="9bdc5-113">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="9bdc5-114">-Smartfqdn parametresiyle, bu kaynağa tahsis edilen genel IP adresi için, komutta belirtilen $customFqdn işaret eden bir DNS PTR kaydı (ters arama) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="9bdc5-115">Önkoşul olarak, $customFqdn (say webapp.contoso.com), $dnsPrefix. $location. cloudapp.azure.com 'e işaret eden bir DNS CNAME kaydı (ileriye-arama) içermelidir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="9bdc5-116">3: ıptag ile yeni bir genel IP adresi oluşturun</span><span class="sxs-lookup"><span data-stu-id="9bdc5-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="9bdc5-117">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="9bdc5-118">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="9bdc5-119">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="9bdc5-120">Kaynak ile ilişkilendirilmiş etiketleri için ıptag kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="9bdc5-121">Iptag New-AzureRmPublicIpTag kullanarak belirtilebilir ve-ıptags aracılığıyla giriş olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="9bdc5-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bdc5-122">PARAMETERS</span></span>

### <span data-ttu-id="9bdc5-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="9bdc5-123">-AllocationMethod</span></span>
<span data-ttu-id="9bdc5-124">Genel IP adresinin tahsis edilmesi yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="9bdc5-125">Bu parametre için kabul edilebilir değerler: statik veya dinamik.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="9bdc5-126">-AsJob</span></span>
<span data-ttu-id="9bdc5-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9bdc5-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bdc5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdc5-128">-DefaultProfile</span></span>
<span data-ttu-id="9bdc5-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bdc5-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="9bdc5-130">-DomainNameLabel</span></span>
<span data-ttu-id="9bdc5-131">Genel bir IP adresi için göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-131">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9bdc5-132">-Force</span></span>
<span data-ttu-id="9bdc5-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bdc5-134">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="9bdc5-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9bdc5-135">Bekleme süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9bdc5-136">-IpAddressVersion</span></span>
<span data-ttu-id="9bdc5-137">IP adresinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-138">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="9bdc5-138">-IpTag</span></span>
<span data-ttu-id="9bdc5-139">Iptag listesi.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-139">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="9bdc5-140">-Location</span></span>
<span data-ttu-id="9bdc5-141">Genel IP adresi oluşturacağınız bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-141">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bdc5-142">-Name</span></span>
<span data-ttu-id="9bdc5-143">Bu cmdlet 'in oluşturduğu ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bdc5-144">-ResourceGroupName</span></span>
<span data-ttu-id="9bdc5-145">Genel IP adresi oluşturacağınız kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-146">-Smarfqdn</span><span class="sxs-lookup"><span data-stu-id="9bdc5-146">-ReverseFqdn</span></span>
<span data-ttu-id="9bdc5-147">Geriye doğru tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="9bdc5-148">-Sku</span></span>
<span data-ttu-id="9bdc5-149">Genel IP SKU adı.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9bdc5-150">-Tag</span></span>
<span data-ttu-id="9bdc5-151">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9bdc5-152">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9bdc5-152">For example:</span></span>

<span data-ttu-id="9bdc5-153">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9bdc5-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-154">-Bölge</span><span class="sxs-lookup"><span data-stu-id="9bdc5-154">-Zone</span></span>
<span data-ttu-id="9bdc5-155">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bdc5-156">-Confirm</span></span>
<span data-ttu-id="9bdc5-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdc5-158">-WhatIf</span></span>
<span data-ttu-id="9bdc5-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bdc5-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdc5-161">CommonParameters</span></span>
<span data-ttu-id="9bdc5-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdc5-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bdc5-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdc5-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bdc5-164">INPUTS</span></span>

### <span data-ttu-id="9bdc5-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9bdc5-165">None</span></span>
<span data-ttu-id="9bdc5-166">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9bdc5-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bdc5-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bdc5-167">OUTPUTS</span></span>

### <span data-ttu-id="9bdc5-168">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9bdc5-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9bdc5-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bdc5-169">NOTES</span></span>

## <span data-ttu-id="9bdc5-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bdc5-170">RELATED LINKS</span></span>

[<span data-ttu-id="9bdc5-171">Get-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9bdc5-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9bdc5-172">Remove-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9bdc5-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9bdc5-173">Set-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9bdc5-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
