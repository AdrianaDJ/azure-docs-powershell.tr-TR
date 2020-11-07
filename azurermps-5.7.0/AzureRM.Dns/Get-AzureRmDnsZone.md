---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763282"
---
# <span data-ttu-id="8be14-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="8be14-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="8be14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be14-102">SYNOPSIS</span></span>
<span data-ttu-id="8be14-103">DNS bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="8be14-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8be14-104">SYNTAX</span></span>

### <span data-ttu-id="8be14-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8be14-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8be14-106">Kaynak</span><span class="sxs-lookup"><span data-stu-id="8be14-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8be14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8be14-107">DESCRIPTION</span></span>
<span data-ttu-id="8be14-108">**Get-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="8be14-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="8be14-109">*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="8be14-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="8be14-110">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="8be14-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="8be14-111">Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be14-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="8be14-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8be14-112">EXAMPLES</span></span>

### <span data-ttu-id="8be14-113">Örnek 1: bölge alma</span><span class="sxs-lookup"><span data-stu-id="8be14-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="8be14-114">Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="8be14-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="8be14-115">Örnek 2: kaynak grubundaki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="8be14-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8be14-116">Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="8be14-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="8be14-117">Örnek 3: abonelikteki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="8be14-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="8be14-118">Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="8be14-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="8be14-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8be14-119">PARAMETERS</span></span>

### <span data-ttu-id="8be14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be14-120">-DefaultProfile</span></span>
<span data-ttu-id="8be14-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8be14-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8be14-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8be14-122">-Name</span></span>
<span data-ttu-id="8be14-123">Alınacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be14-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="8be14-124">*Name* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak GRUBUNDAKI tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="8be14-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="8be14-125">*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="8be14-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="8be14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be14-126">-ResourceGroupName</span></span>
<span data-ttu-id="8be14-127">Alınacak DNS bölgesini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be14-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="8be14-128">*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.</span><span class="sxs-lookup"><span data-stu-id="8be14-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="8be14-129">Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="8be14-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="8be14-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be14-130">CommonParameters</span></span>
<span data-ttu-id="8be14-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8be14-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be14-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be14-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be14-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8be14-133">INPUTS</span></span>

### <span data-ttu-id="8be14-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8be14-134">None</span></span>
<span data-ttu-id="8be14-135">Bu cmdlet girişi boru yapmanıza izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="8be14-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="8be14-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8be14-136">OUTPUTS</span></span>

### <span data-ttu-id="8be14-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="8be14-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="8be14-138">Bu cmdlet, DNS bölgesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8be14-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="8be14-139">Bölge adı belirtilmezse, bölge nesneleri dizisi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="8be14-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="8be14-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8be14-140">NOTES</span></span>

## <span data-ttu-id="8be14-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8be14-141">RELATED LINKS</span></span>

[<span data-ttu-id="8be14-142">Yeni-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="8be14-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="8be14-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="8be14-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="8be14-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="8be14-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)