---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109642"
---
# <span data-ttu-id="105f5-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="105f5-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="105f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105f5-102">SYNOPSIS</span></span>
<span data-ttu-id="105f5-103">DNS bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="105f5-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="105f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="105f5-104">SYNTAX</span></span>

### <span data-ttu-id="105f5-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="105f5-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="105f5-106">Kaynak</span><span class="sxs-lookup"><span data-stu-id="105f5-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="105f5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="105f5-107">DESCRIPTION</span></span>
<span data-ttu-id="105f5-108">**Get-AzDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="105f5-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="105f5-109">*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="105f5-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="105f5-110">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="105f5-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="105f5-111">Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="105f5-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="105f5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="105f5-112">EXAMPLES</span></span>

### <span data-ttu-id="105f5-113">Örnek 1: bölge alma</span><span class="sxs-lookup"><span data-stu-id="105f5-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="105f5-114">Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="105f5-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="105f5-115">Örnek 2: kaynak grubundaki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="105f5-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="105f5-116">Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="105f5-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="105f5-117">Örnek 3: abonelikteki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="105f5-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="105f5-118">Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="105f5-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="105f5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="105f5-119">PARAMETERS</span></span>

### <span data-ttu-id="105f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105f5-120">-DefaultProfile</span></span>
<span data-ttu-id="105f5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="105f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="105f5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="105f5-122">-Name</span></span>
<span data-ttu-id="105f5-123">Alınacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="105f5-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="105f5-124">*Name* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak GRUBUNDAKI tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="105f5-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="105f5-125">*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="105f5-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="105f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="105f5-127">Alınacak DNS bölgesini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="105f5-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="105f5-128">*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.</span><span class="sxs-lookup"><span data-stu-id="105f5-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="105f5-129">Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="105f5-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105f5-130">CommonParameters</span></span>
<span data-ttu-id="105f5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="105f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105f5-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105f5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105f5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="105f5-133">INPUTS</span></span>

### <span data-ttu-id="105f5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="105f5-134">System.String</span></span>

## <span data-ttu-id="105f5-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="105f5-135">OUTPUTS</span></span>

### <span data-ttu-id="105f5-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="105f5-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="105f5-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="105f5-137">NOTES</span></span>

## <span data-ttu-id="105f5-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="105f5-138">RELATED LINKS</span></span>

[<span data-ttu-id="105f5-139">Yeni-Azdnzone</span><span class="sxs-lookup"><span data-stu-id="105f5-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="105f5-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="105f5-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="105f5-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="105f5-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
