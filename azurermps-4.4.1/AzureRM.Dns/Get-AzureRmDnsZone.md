---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764065"
---
# <span data-ttu-id="a3e6f-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3e6f-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="a3e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e6f-103">DNS bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3e6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3e6f-104">SYNTAX</span></span>

### <span data-ttu-id="a3e6f-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3e6f-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e6f-106">Kaynak</span><span class="sxs-lookup"><span data-stu-id="a3e6f-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3e6f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3e6f-107">DESCRIPTION</span></span>
<span data-ttu-id="a3e6f-108">**Get-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="a3e6f-109">*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="a3e6f-110">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="a3e6f-111">Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="a3e6f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3e6f-112">EXAMPLES</span></span>

### <span data-ttu-id="a3e6f-113">Örnek 1: bölge alma</span><span class="sxs-lookup"><span data-stu-id="a3e6f-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="a3e6f-114">Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a3e6f-115">Örnek 2: kaynak grubundaki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="a3e6f-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a3e6f-116">Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="a3e6f-117">Örnek 3: abonelikteki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="a3e6f-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="a3e6f-118">Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="a3e6f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3e6f-119">PARAMETERS</span></span>

### <span data-ttu-id="a3e6f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3e6f-120">-Name</span></span>
<span data-ttu-id="a3e6f-121">Alınacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="a3e6f-122">*Name* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak GRUBUNDAKI tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="a3e6f-123">*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="a3e6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3e6f-125">Alınacak DNS bölgesini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="a3e6f-126">*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="a3e6f-127">Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="a3e6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e6f-128">-DefaultProfile</span></span>
<span data-ttu-id="a3e6f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e6f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e6f-130">CommonParameters</span></span>
<span data-ttu-id="a3e6f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e6f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e6f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e6f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3e6f-133">INPUTS</span></span>

### <span data-ttu-id="a3e6f-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a3e6f-134">None</span></span>
<span data-ttu-id="a3e6f-135">Bu cmdlet girişi boru yapmanıza izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="a3e6f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3e6f-136">OUTPUTS</span></span>

### <span data-ttu-id="a3e6f-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a3e6f-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a3e6f-138">Bu cmdlet, DNS bölgesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="a3e6f-139">Bölge adı belirtilmezse, bölge nesneleri dizisi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a3e6f-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="a3e6f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3e6f-140">NOTES</span></span>

## <span data-ttu-id="a3e6f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3e6f-141">RELATED LINKS</span></span>

[<span data-ttu-id="a3e6f-142">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3e6f-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="a3e6f-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3e6f-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="a3e6f-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a3e6f-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
