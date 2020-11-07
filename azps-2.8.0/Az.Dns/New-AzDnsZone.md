---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 101440e65fbc0bb21311757a8792a2d45f855364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752032"
---
# <span data-ttu-id="04ef0-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="04ef0-101">New-AzDnsZone</span></span>

## <span data-ttu-id="04ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="04ef0-103">Yeni bir DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04ef0-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="04ef0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04ef0-104">SYNTAX</span></span>

### <span data-ttu-id="04ef0-105">Kimlikler (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04ef0-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ef0-106">Adına</span><span class="sxs-lookup"><span data-stu-id="04ef0-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ef0-107">Nesnelere</span><span class="sxs-lookup"><span data-stu-id="04ef0-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ef0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="04ef0-108">DESCRIPTION</span></span>
<span data-ttu-id="04ef0-109">**New-AzDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04ef0-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="04ef0-110">*Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="04ef0-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="04ef0-111">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="04ef0-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="04ef0-112">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04ef0-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="04ef0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04ef0-113">EXAMPLES</span></span>

### <span data-ttu-id="04ef0-114">Örnek 1: DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="04ef0-115">Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="04ef0-116">Örnek 2: sanal ağ kimlikleri belirterek özel bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="04ef0-117">Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağı (ID 'sini belirterek) ile oluşturur ve ardından $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="04ef0-118">Örnek 3: sanal ağ nesneleri belirterek özel bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="04ef0-119">Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağıyla ($ResVirtualNetwork değişkeni ile başvurulan) oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="04ef0-120">Örnek 4: üst bölge adını belirterek temsilci ile bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="04ef0-121">Bu komut, mychild.zone.com adında yeni bir alt DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="04ef0-122">Ayrıca, zone.com adlı üst DNS bölgesinde, alt bölgeyle aynı abonelikte ve kaynak grubunda yer alan temsilci ekler.</span><span class="sxs-lookup"><span data-stu-id="04ef0-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="04ef0-123">Örnek 5: üst bölge kimliğini belirterek temsilci ile bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="04ef0-124">Bu komut, mychild.zone.com adında yeni bir alt DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="04ef0-125">Ayrıca, kaynak grubundaki zone.com adlı üst DNS bölgesinde temsilci ekler ve diğer RG sağlanan abonelik, alt bölgenin oluşturulduğu ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="04ef0-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="04ef0-126">Örnek 6: üst bölge nesnesini belirterek temsilyle bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="04ef0-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="04ef0-127">Bu komut, mychild.zone.com adında yeni bir alt DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="04ef0-128">Ayrıca zone.com adındaki üst DNS bölgesinde, ParentZone nesnesinde geçti olarak temsilci ekler</span><span class="sxs-lookup"><span data-stu-id="04ef0-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="04ef0-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04ef0-129">PARAMETERS</span></span>

### <span data-ttu-id="04ef0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ef0-130">-DefaultProfile</span></span>
<span data-ttu-id="04ef0-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="04ef0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04ef0-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="04ef0-132">-Name</span></span>
<span data-ttu-id="04ef0-133">Oluşturulacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="04ef0-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="04ef0-134">-ParentZone</span></span>
<span data-ttu-id="04ef0-135">Temsilci eklenecek üst bölgenin tam adı (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="04ef0-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ef0-136">-Parentzoneıd</span><span class="sxs-lookup"><span data-stu-id="04ef0-136">-ParentZoneId</span></span>
<span data-ttu-id="04ef0-137">Üst bölgenin Temsilci (Sonlandırıcı noktası olmadan) eklemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="04ef0-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ef0-138">-Parentbölgeadı</span><span class="sxs-lookup"><span data-stu-id="04ef0-138">-ParentZoneName</span></span>
<span data-ttu-id="04ef0-139">Temsilci eklenecek üst bölgenin tam adı (Sonlandırıcı nokta olmadan).</span><span class="sxs-lookup"><span data-stu-id="04ef0-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ef0-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04ef0-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="04ef0-141">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="04ef0-142">-Registrationvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="04ef0-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="04ef0-143">Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="04ef0-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04ef0-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="04ef0-145">Bu DNS bölgesindeki kayıtları çözümleyebileceğiniz sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="04ef0-146">-Resolutionvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="04ef0-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="04ef0-147">Bu DNS bölgesindeki kayıtları çözümleyemeyecek sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="04ef0-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ef0-148">-ResourceGroupName</span></span>
<span data-ttu-id="04ef0-149">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="04ef0-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="04ef0-150">-Tag</span></span>
<span data-ttu-id="04ef0-151">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="04ef0-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04ef0-152">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="04ef0-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ef0-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="04ef0-153">-ZoneType</span></span>
<span data-ttu-id="04ef0-154">Bölgenin türü, genel veya özel.</span><span class="sxs-lookup"><span data-stu-id="04ef0-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="04ef0-155">Türü olmayan veya ortak türü olmayan bölgeler, DNS hiyerarşisinde kullanılmak üzere ortak DNS hizmet sunma düzleminde sağlanır.</span><span class="sxs-lookup"><span data-stu-id="04ef0-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="04ef0-156">Özel türündeki bölgeler yalnızca ilişkili sanal ağlar kümesiyle (Bu özellik önizlemede) görünür.</span><span class="sxs-lookup"><span data-stu-id="04ef0-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="04ef0-157">Bu özellik bir bölge için değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="04ef0-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ef0-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="04ef0-158">-Confirm</span></span>
<span data-ttu-id="04ef0-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04ef0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ef0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ef0-160">-WhatIf</span></span>
<span data-ttu-id="04ef0-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04ef0-162">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04ef0-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04ef0-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04ef0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ef0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ef0-164">CommonParameters</span></span>
<span data-ttu-id="04ef0-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04ef0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ef0-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ef0-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ef0-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04ef0-167">INPUTS</span></span>

### <span data-ttu-id="04ef0-168">System. String</span><span class="sxs-lookup"><span data-stu-id="04ef0-168">System.String</span></span>

### <span data-ttu-id="04ef0-169">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. modeller. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="04ef0-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="04ef0-170">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="04ef0-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04ef0-171">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="04ef0-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04ef0-172">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="04ef0-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="04ef0-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04ef0-173">OUTPUTS</span></span>

### <span data-ttu-id="04ef0-174">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="04ef0-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="04ef0-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04ef0-175">NOTES</span></span>
<span data-ttu-id="04ef0-176">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="04ef0-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="04ef0-177">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="04ef0-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="04ef0-178">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="04ef0-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="04ef0-179">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="04ef0-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="04ef0-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04ef0-180">RELATED LINKS</span></span>

[<span data-ttu-id="04ef0-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="04ef0-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="04ef0-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="04ef0-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="04ef0-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="04ef0-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)