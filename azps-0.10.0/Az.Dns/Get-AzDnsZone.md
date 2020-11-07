---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936732"
---
# <span data-ttu-id="7d1b4-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7d1b4-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="7d1b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1b4-103">DNS bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="7d1b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d1b4-104">SYNTAX</span></span>

### <span data-ttu-id="7d1b4-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d1b4-105">Default (Default)</span></span>
```
Get-AzDnsZone [<CommonParameters>]
```

### <span data-ttu-id="7d1b4-106">Kaynak</span><span class="sxs-lookup"><span data-stu-id="7d1b4-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="7d1b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d1b4-107">DESCRIPTION</span></span>
<span data-ttu-id="7d1b4-108">**Get-AzDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="7d1b4-109">*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="7d1b4-110">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="7d1b4-111">Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="7d1b4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d1b4-112">EXAMPLES</span></span>

### <span data-ttu-id="7d1b4-113">Örnek 1: bölge alma</span><span class="sxs-lookup"><span data-stu-id="7d1b4-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="7d1b4-114">Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="7d1b4-115">Örnek 2: kaynak grubundaki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="7d1b4-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7d1b4-116">Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="7d1b4-117">Örnek 3: abonelikteki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="7d1b4-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="7d1b4-118">Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="7d1b4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d1b4-119">PARAMETERS</span></span>

### <span data-ttu-id="7d1b4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d1b4-120">-Name</span></span>
<span data-ttu-id="7d1b4-121">Alınacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="7d1b4-122">*Name* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak GRUBUNDAKI tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="7d1b4-123">*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d1b4-125">Alınacak DNS bölgesini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="7d1b4-126">*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="7d1b4-127">Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d1b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1b4-128">CommonParameters</span></span>
<span data-ttu-id="7d1b4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1b4-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1b4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1b4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d1b4-131">INPUTS</span></span>

### <span data-ttu-id="7d1b4-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7d1b4-132">None</span></span>
<span data-ttu-id="7d1b4-133">Bu cmdlet girişi boru yapmanıza izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="7d1b4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d1b4-134">OUTPUTS</span></span>

### <span data-ttu-id="7d1b4-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="7d1b4-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="7d1b4-136">Bu cmdlet, DNS bölgesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="7d1b4-137">Bölge adı belirtilmezse, bölge nesneleri dizisi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="7d1b4-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d1b4-138">NOTES</span></span>

## <span data-ttu-id="7d1b4-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d1b4-139">RELATED LINKS</span></span>

[<span data-ttu-id="7d1b4-140">Yeni-Azdnzone</span><span class="sxs-lookup"><span data-stu-id="7d1b4-140">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="7d1b4-141">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7d1b4-141">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="7d1b4-142">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7d1b4-142">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
