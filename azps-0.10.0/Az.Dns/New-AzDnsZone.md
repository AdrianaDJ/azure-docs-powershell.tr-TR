---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936721"
---
# <span data-ttu-id="811e0-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="811e0-101">New-AzDnsZone</span></span>

## <span data-ttu-id="811e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="811e0-102">SYNOPSIS</span></span>
<span data-ttu-id="811e0-103">Yeni bir DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="811e0-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="811e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="811e0-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="811e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="811e0-105">DESCRIPTION</span></span>
<span data-ttu-id="811e0-106">**New-AzDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="811e0-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="811e0-107">*Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="811e0-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="811e0-108">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="811e0-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="811e0-109">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="811e0-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="811e0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="811e0-110">EXAMPLES</span></span>

### <span data-ttu-id="811e0-111">Örnek 1: DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="811e0-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="811e0-112">Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="811e0-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="811e0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="811e0-113">PARAMETERS</span></span>

### <span data-ttu-id="811e0-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="811e0-114">-Name</span></span>
<span data-ttu-id="811e0-115">Oluşturulacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="811e0-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="811e0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="811e0-116">-ResourceGroupName</span></span>
<span data-ttu-id="811e0-117">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="811e0-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="811e0-118">Etiketli</span><span class="sxs-lookup"><span data-stu-id="811e0-118">-Tag</span></span>
<span data-ttu-id="811e0-119">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="811e0-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="811e0-120">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="811e0-120">For example:</span></span>

<span data-ttu-id="811e0-121">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="811e0-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="811e0-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="811e0-122">-Confirm</span></span>
<span data-ttu-id="811e0-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="811e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811e0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811e0-124">-WhatIf</span></span>
<span data-ttu-id="811e0-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="811e0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="811e0-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="811e0-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="811e0-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="811e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811e0-128">CommonParameters</span></span>
<span data-ttu-id="811e0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="811e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811e0-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="811e0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811e0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="811e0-131">INPUTS</span></span>

### <span data-ttu-id="811e0-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="811e0-132">None</span></span>

<span data-ttu-id="811e0-133">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="811e0-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="811e0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="811e0-134">OUTPUTS</span></span>

### <span data-ttu-id="811e0-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="811e0-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="811e0-136">Bu cmdlet, yeni DNS bölgesini temsil eden bir Microsoft. Azure. Commands. DNS. DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="811e0-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="811e0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="811e0-137">NOTES</span></span>
<span data-ttu-id="811e0-138">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="811e0-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="811e0-139">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="811e0-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="811e0-140">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="811e0-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="811e0-141">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="811e0-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="811e0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="811e0-142">RELATED LINKS</span></span>

[<span data-ttu-id="811e0-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="811e0-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="811e0-144">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="811e0-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="811e0-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="811e0-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)