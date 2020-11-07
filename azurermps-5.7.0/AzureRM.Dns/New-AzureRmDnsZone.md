---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762647"
---
# <span data-ttu-id="d154e-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d154e-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="d154e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d154e-102">SYNOPSIS</span></span>
<span data-ttu-id="d154e-103">Yeni bir DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d154e-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d154e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d154e-104">SYNTAX</span></span>

### <span data-ttu-id="d154e-105">Kimlikler (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d154e-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d154e-106">Nesnelere</span><span class="sxs-lookup"><span data-stu-id="d154e-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d154e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d154e-107">DESCRIPTION</span></span>
<span data-ttu-id="d154e-108">**Yeni-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d154e-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="d154e-109">*Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="d154e-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="d154e-110">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzureRmDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d154e-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="d154e-111">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d154e-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d154e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d154e-112">EXAMPLES</span></span>

### <span data-ttu-id="d154e-113">Örnek 1: DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d154e-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d154e-114">Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d154e-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d154e-115">Örnek 2: sanal ağ kimlikleri belirterek özel bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d154e-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="d154e-116">Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağı (ID 'sini belirterek) ile oluşturur ve ardından $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d154e-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="d154e-117">Örnek 3: sanal ağ nesneleri belirterek özel bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d154e-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="d154e-118">Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağıyla ($ResVirtualNetwork değişkeni ile başvurulan) oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d154e-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="d154e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d154e-119">PARAMETERS</span></span>

### <span data-ttu-id="d154e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d154e-120">-DefaultProfile</span></span>
<span data-ttu-id="d154e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d154e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d154e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d154e-122">-Name</span></span>
<span data-ttu-id="d154e-123">Oluşturulacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d154e-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="d154e-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d154e-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="d154e-125">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d154e-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-126">-Registrationvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="d154e-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="d154e-127">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d154e-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d154e-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="d154e-129">Bu DNS bölgesindeki kayıtları çözümleyebileceğiniz sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d154e-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-130">-Resolutionvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="d154e-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="d154e-131">Bu DNS bölgesindeki kayıtları çözümleyemeyecek sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d154e-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d154e-132">-ResourceGroupName</span></span>
<span data-ttu-id="d154e-133">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d154e-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="d154e-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d154e-134">-Tag</span></span>
<span data-ttu-id="d154e-135">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d154e-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d154e-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d154e-136">For example:</span></span>

<span data-ttu-id="d154e-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d154e-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-138">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="d154e-138">-ZoneType</span></span>
<span data-ttu-id="d154e-139">Bölgenin türü, genel veya özel.</span><span class="sxs-lookup"><span data-stu-id="d154e-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="d154e-140">Türü olmayan veya ortak türü olmayan bölgeler, DNS hiyerarşisinde kullanılmak üzere ortak DNS hizmet sunma düzleminde sağlanır.</span><span class="sxs-lookup"><span data-stu-id="d154e-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="d154e-141">Özel türündeki bölgeler yalnızca ilişkili sanal ağlar kümesiyle (Bu özellik önizlemede) görünür.</span><span class="sxs-lookup"><span data-stu-id="d154e-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="d154e-142">Bu özellik bir bölge için değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="d154e-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d154e-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="d154e-143">-Confirm</span></span>
<span data-ttu-id="d154e-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d154e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d154e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d154e-145">-WhatIf</span></span>
<span data-ttu-id="d154e-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d154e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d154e-147">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d154e-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d154e-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d154e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d154e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d154e-149">CommonParameters</span></span>
<span data-ttu-id="d154e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d154e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d154e-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d154e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d154e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d154e-152">INPUTS</span></span>

### <span data-ttu-id="d154e-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d154e-153">None</span></span>
<span data-ttu-id="d154e-154">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d154e-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="d154e-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d154e-155">OUTPUTS</span></span>

### <span data-ttu-id="d154e-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="d154e-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d154e-157">Bu cmdlet, yeni DNS bölgesini temsil eden bir Microsoft. Azure. Commands. DNS. DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="d154e-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="d154e-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d154e-158">NOTES</span></span>
<span data-ttu-id="d154e-159">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="d154e-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d154e-160">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="d154e-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="d154e-161">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="d154e-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d154e-162">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="d154e-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d154e-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d154e-163">RELATED LINKS</span></span>

[<span data-ttu-id="d154e-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d154e-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="d154e-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d154e-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d154e-166">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="d154e-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
