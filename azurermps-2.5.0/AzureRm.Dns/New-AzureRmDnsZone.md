---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46b14399d1cae624f4735111d809702cfd14180e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939401"
---
# <span data-ttu-id="5b649-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b649-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="5b649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b649-102">SYNOPSIS</span></span>
<span data-ttu-id="5b649-103">Yeni bir DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b649-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b649-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b649-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b649-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b649-105">DESCRIPTION</span></span>
<span data-ttu-id="5b649-106">**Yeni-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b649-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="5b649-107">*Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="5b649-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="5b649-108">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzureRmDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b649-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="5b649-109">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b649-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5b649-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b649-110">EXAMPLES</span></span>

### <span data-ttu-id="5b649-111">Örnek 1: DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b649-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5b649-112">Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b649-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="5b649-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b649-113">PARAMETERS</span></span>

### <span data-ttu-id="5b649-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b649-114">-Name</span></span>
<span data-ttu-id="5b649-115">Oluşturulacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b649-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="5b649-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b649-116">-ResourceGroupName</span></span>
<span data-ttu-id="5b649-117">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b649-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="5b649-118">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5b649-118">-Tag</span></span>
<span data-ttu-id="5b649-119">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5b649-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b649-120">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="5b649-120">For example:</span></span>

<span data-ttu-id="5b649-121">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5b649-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b649-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b649-122">-Confirm</span></span>
<span data-ttu-id="5b649-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b649-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b649-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b649-124">-WhatIf</span></span>
<span data-ttu-id="5b649-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b649-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b649-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b649-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b649-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b649-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b649-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b649-128">CommonParameters</span></span>
<span data-ttu-id="5b649-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b649-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b649-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b649-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b649-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b649-131">INPUTS</span></span>

### <span data-ttu-id="5b649-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b649-132">None</span></span>

<span data-ttu-id="5b649-133">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5b649-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="5b649-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b649-134">OUTPUTS</span></span>

### <span data-ttu-id="5b649-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="5b649-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="5b649-136">Bu cmdlet, yeni DNS bölgesini temsil eden bir Microsoft. Azure. Commands. DNS. DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5b649-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="5b649-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b649-137">NOTES</span></span>
<span data-ttu-id="5b649-138">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="5b649-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5b649-139">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="5b649-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="5b649-140">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b649-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5b649-141">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="5b649-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5b649-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b649-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b649-143">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b649-143">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="5b649-144">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5b649-144">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="5b649-145">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b649-145">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
