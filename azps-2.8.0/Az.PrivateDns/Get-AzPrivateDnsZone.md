---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 659281d1f78ea984a3db30817d15a6e92f31cbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933091"
---
# <span data-ttu-id="11749-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11749-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="11749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11749-102">SYNOPSIS</span></span>
<span data-ttu-id="11749-103">Özel bir DNS bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="11749-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="11749-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11749-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11749-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11749-105">DESCRIPTION</span></span>
<span data-ttu-id="11749-106">**Get-AzPrivateDnsZone** cmdlet 'i belirtilen kaynak grubundan özel bir etki alanı adı SISTEMI (DNS) bölgesi alır.</span><span class="sxs-lookup"><span data-stu-id="11749-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="11749-107">*Name* parametresini belirtirseniz, tek bir **PrivateDnsZone** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="11749-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="11749-108">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="11749-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="11749-109">Bölgeyi güncelleştirmek için **PrivateDnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11749-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="11749-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11749-110">EXAMPLES</span></span>

### <span data-ttu-id="11749-111">Örnek 1: bölge alma</span><span class="sxs-lookup"><span data-stu-id="11749-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="11749-112">Örnek 2: kaynak grubundaki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="11749-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="11749-113">Bu örnekte, belirtilen kaynak grubundaki özel DNS bölgelerinin tümü alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="11749-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="11749-114">Örnek 3: abonelikteki tüm bölgeleri alma</span><span class="sxs-lookup"><span data-stu-id="11749-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="11749-115">Bu örnekte, geçerli Azure aboneliğindeki tüm özel DNS bölgeleri alınır ve $Zones değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="11749-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="11749-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11749-116">PARAMETERS</span></span>

### <span data-ttu-id="11749-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11749-117">-DefaultProfile</span></span>
<span data-ttu-id="11749-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="11749-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11749-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="11749-119">-Name</span></span>
<span data-ttu-id="11749-120">Alınacak özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11749-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="11749-121">*Ad* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak grubundaki tüm özel DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="11749-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="11749-122">*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm özel DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="11749-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11749-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11749-123">-ResourceGroupName</span></span>
<span data-ttu-id="11749-124">Alınacak özel DNS bölgesini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11749-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="11749-125">*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.</span><span class="sxs-lookup"><span data-stu-id="11749-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="11749-126">Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm özel DNS bölgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="11749-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11749-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11749-127">CommonParameters</span></span>
<span data-ttu-id="11749-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11749-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11749-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11749-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11749-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11749-130">INPUTS</span></span>

### <span data-ttu-id="11749-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="11749-131">None</span></span>

## <span data-ttu-id="11749-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11749-132">OUTPUTS</span></span>

### <span data-ttu-id="11749-133">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11749-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="11749-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11749-134">NOTES</span></span>

## <span data-ttu-id="11749-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11749-135">RELATED LINKS</span></span>

[<span data-ttu-id="11749-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11749-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="11749-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11749-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="11749-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="11749-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)