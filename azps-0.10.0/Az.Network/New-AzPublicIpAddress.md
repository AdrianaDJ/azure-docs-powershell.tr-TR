---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935366"
---
# <span data-ttu-id="09808-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09808-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="09808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09808-102">SYNOPSIS</span></span>
<span data-ttu-id="09808-103">Genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="09808-103">Creates a public IP address.</span></span>

## <span data-ttu-id="09808-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09808-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09808-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09808-105">DESCRIPTION</span></span>
<span data-ttu-id="09808-106">**New-Azpublicıpaddress** cmdlet 'i genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="09808-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="09808-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09808-107">EXAMPLES</span></span>

### <span data-ttu-id="09808-108">1: yeni bir genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="09808-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="09808-109">Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09808-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="09808-110">-AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="09808-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="09808-111">' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="09808-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="09808-112">2: ters FQDN ile genel IP adresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="09808-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="09808-113">Bu komut yeni bir genel IP adresi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="09808-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="09808-114">-Smartfqdn parametresiyle, bu kaynağa tahsis edilen genel IP adresi için, komutta belirtilen $customFqdn işaret eden bir DNS PTR kaydı (ters arama) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09808-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="09808-115">Önkoşul olarak, $customFqdn (say webapp.contoso.com), $dnsPrefix. $location. cloudapp.azure.com 'e işaret eden bir DNS CNAME kaydı (ileriye-arama) içermelidir.</span><span class="sxs-lookup"><span data-stu-id="09808-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="09808-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09808-116">PARAMETERS</span></span>

### <span data-ttu-id="09808-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="09808-117">-AllocationMethod</span></span>
<span data-ttu-id="09808-118">Genel IP adresinin tahsis edilmesi yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="09808-119">Bu parametre için kabul edilebilir değerler: statik veya dinamik.</span><span class="sxs-lookup"><span data-stu-id="09808-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="09808-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="09808-120">-AsJob</span></span>
<span data-ttu-id="09808-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="09808-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09808-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09808-122">-DefaultProfile</span></span>
<span data-ttu-id="09808-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09808-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09808-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="09808-124">-DomainNameLabel</span></span>
<span data-ttu-id="09808-125">Genel bir IP adresi için göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="09808-126">-Force</span><span class="sxs-lookup"><span data-stu-id="09808-126">-Force</span></span>
<span data-ttu-id="09808-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="09808-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09808-128">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="09808-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="09808-129">Bekleme süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="09808-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="09808-130">-IpAddressVersion</span></span>
<span data-ttu-id="09808-131">IP adresinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="09808-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="09808-132">-Location</span></span>
<span data-ttu-id="09808-133">Genel IP adresi oluşturacağınız bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="09808-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="09808-134">-Name</span></span>
<span data-ttu-id="09808-135">Bu cmdlet 'in oluşturduğu ortak IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="09808-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09808-136">-ResourceGroupName</span></span>
<span data-ttu-id="09808-137">Genel IP adresi oluşturacağınız kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="09808-138">-Smarfqdn</span><span class="sxs-lookup"><span data-stu-id="09808-138">-ReverseFqdn</span></span>
<span data-ttu-id="09808-139">Geriye doğru tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="09808-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="09808-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="09808-140">-Sku</span></span>
<span data-ttu-id="09808-141">Genel IP SKU adı.</span><span class="sxs-lookup"><span data-stu-id="09808-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="09808-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="09808-142">-Tag</span></span>
<span data-ttu-id="09808-143">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="09808-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="09808-144">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="09808-144">For example:</span></span>

<span data-ttu-id="09808-145">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="09808-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="09808-146">-Bölge</span><span class="sxs-lookup"><span data-stu-id="09808-146">-Zone</span></span>
<span data-ttu-id="09808-147">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="09808-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="09808-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="09808-148">-Confirm</span></span>
<span data-ttu-id="09808-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09808-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09808-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09808-150">-WhatIf</span></span>
<span data-ttu-id="09808-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09808-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09808-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09808-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09808-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09808-153">CommonParameters</span></span>
<span data-ttu-id="09808-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09808-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09808-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09808-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09808-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09808-156">INPUTS</span></span>

## <span data-ttu-id="09808-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09808-157">OUTPUTS</span></span>

### <span data-ttu-id="09808-158">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="09808-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="09808-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09808-159">NOTES</span></span>

## <span data-ttu-id="09808-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09808-160">RELATED LINKS</span></span>

[<span data-ttu-id="09808-161">Get-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="09808-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="09808-162">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="09808-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="09808-163">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="09808-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
