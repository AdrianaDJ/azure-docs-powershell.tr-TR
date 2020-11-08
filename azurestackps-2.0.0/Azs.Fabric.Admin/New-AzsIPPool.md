---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936021"
---
# <span data-ttu-id="122ec-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="122ec-101">New-AzsIPPool</span></span>

## <span data-ttu-id="122ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122ec-102">SYNOPSIS</span></span>
<span data-ttu-id="122ec-103">IP havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="122ec-103">Create an IP pool.</span></span>
<span data-ttu-id="122ec-104">Bir IP havuzu oluşturulduktan sonra silinemez.</span><span class="sxs-lookup"><span data-stu-id="122ec-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="122ec-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="122ec-105">SYNTAX</span></span>

### <span data-ttu-id="122ec-106">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="122ec-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="122ec-107">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="122ec-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="122ec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="122ec-108">DESCRIPTION</span></span>
<span data-ttu-id="122ec-109">IP havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="122ec-109">Create an IP pool.</span></span>
<span data-ttu-id="122ec-110">Bir IP havuzu oluşturulduktan sonra silinemez.</span><span class="sxs-lookup"><span data-stu-id="122ec-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="122ec-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="122ec-111">EXAMPLES</span></span>

### <span data-ttu-id="122ec-112">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="122ec-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="122ec-113">Yeni bir IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="122ec-113">Create a new IP pool.</span></span>



## <span data-ttu-id="122ec-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="122ec-114">PARAMETERS</span></span>

### <span data-ttu-id="122ec-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="122ec-115">-AddressPrefix</span></span>
<span data-ttu-id="122ec-116">Adres öneki.</span><span class="sxs-lookup"><span data-stu-id="122ec-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="122ec-117">-AsJob</span></span>
<span data-ttu-id="122ec-118">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="122ec-118">Run the command as a job</span></span>

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

### <span data-ttu-id="122ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122ec-119">-DefaultProfile</span></span>
<span data-ttu-id="122ec-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="122ec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-121">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="122ec-121">-EndIPAddress</span></span>
<span data-ttu-id="122ec-122">Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="122ec-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="122ec-123">-Location</span></span>
<span data-ttu-id="122ec-124">Kaynağın bulunduğu bölge.</span><span class="sxs-lookup"><span data-stu-id="122ec-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="122ec-125">-Name</span></span>
<span data-ttu-id="122ec-126">IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="122ec-126">IP pool name.</span></span>

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

### <span data-ttu-id="122ec-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="122ec-127">-NoWait</span></span>
<span data-ttu-id="122ec-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="122ec-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="122ec-129">-Numberofallocatedıaddress</span><span class="sxs-lookup"><span data-stu-id="122ec-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="122ec-130">Ayrılan IP adreslerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-131">-Numberofıpaddress</span><span class="sxs-lookup"><span data-stu-id="122ec-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="122ec-132">Toplam IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-133">-Numberofıpadressesıntransition</span><span class="sxs-lookup"><span data-stu-id="122ec-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="122ec-134">Geçiş sırasında geçerli IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-135">-Havuz</span><span class="sxs-lookup"><span data-stu-id="122ec-135">-Pool</span></span>
<span data-ttu-id="122ec-136">Bu kaynak, alt ağ içindeki düğümler için adreslerin ayrıldığı IP adresi aralığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="122ec-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="122ec-137">Oluşturmak için, havuz özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="122ec-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122ec-138">-ResourceGroupName</span></span>
<span data-ttu-id="122ec-139">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="122ec-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-140">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="122ec-140">-StartIPAddress</span></span>
<span data-ttu-id="122ec-141">Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="122ec-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="122ec-142">-SubscriptionId</span></span>
<span data-ttu-id="122ec-143">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="122ec-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="122ec-144">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="122ec-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="122ec-145">-Tag</span></span>
<span data-ttu-id="122ec-146">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="122ec-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="122ec-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="122ec-147">-Confirm</span></span>
<span data-ttu-id="122ec-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="122ec-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="122ec-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122ec-149">-WhatIf</span></span>
<span data-ttu-id="122ec-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="122ec-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="122ec-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="122ec-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="122ec-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122ec-152">CommonParameters</span></span>
<span data-ttu-id="122ec-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="122ec-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122ec-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="122ec-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122ec-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="122ec-155">INPUTS</span></span>

### <span data-ttu-id="122ec-156">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıippool</span><span class="sxs-lookup"><span data-stu-id="122ec-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="122ec-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="122ec-157">OUTPUTS</span></span>

### <span data-ttu-id="122ec-158">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıippool</span><span class="sxs-lookup"><span data-stu-id="122ec-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="122ec-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="122ec-159">NOTES</span></span>

<span data-ttu-id="122ec-160">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="122ec-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="122ec-161">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="122ec-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="122ec-162">Havuz <IIPPool> : Bu kaynak, alt ağ içindeki düğümler için adreslerin AYRıLDıĞı IP adresi aralığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="122ec-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="122ec-163">`[Location <String>]`: Kaynağın bulunduğu bölge.</span><span class="sxs-lookup"><span data-stu-id="122ec-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="122ec-164">`[Tag <IResourceTags>]`: Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="122ec-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="122ec-165">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="122ec-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="122ec-166">`[AddressPrefix <String>]`: Adres öneki.</span><span class="sxs-lookup"><span data-stu-id="122ec-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="122ec-167">`[EndIPAddress <String>]`: Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="122ec-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="122ec-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Ayrılan IP adreslerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="122ec-169">`[NumberOfIPAddresses <Int64?>]`: IP adreslerinin toplam sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="122ec-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Geçiş sırasında geçerli IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="122ec-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="122ec-171">`[StartIPAddress <String>]`: Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="122ec-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="122ec-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="122ec-172">RELATED LINKS</span></span>
