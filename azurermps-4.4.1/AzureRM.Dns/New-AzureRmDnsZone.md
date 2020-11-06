---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592626"
---
# <span data-ttu-id="336f5-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="336f5-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="336f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="336f5-102">SYNOPSIS</span></span>
<span data-ttu-id="336f5-103">Yeni bir DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="336f5-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="336f5-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="336f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="336f5-105">DESCRIPTION</span></span>
<span data-ttu-id="336f5-106">**Yeni-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="336f5-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="336f5-107">*Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="336f5-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="336f5-108">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzureRmDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="336f5-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="336f5-109">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="336f5-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="336f5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="336f5-110">EXAMPLES</span></span>

### <span data-ttu-id="336f5-111">Örnek 1: DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="336f5-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="336f5-112">Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="336f5-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="336f5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="336f5-113">PARAMETERS</span></span>

### <span data-ttu-id="336f5-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="336f5-114">-Name</span></span>
<span data-ttu-id="336f5-115">Oluşturulacak DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="336f5-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="336f5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336f5-116">-ResourceGroupName</span></span>
<span data-ttu-id="336f5-117">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="336f5-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="336f5-118">Etiketli</span><span class="sxs-lookup"><span data-stu-id="336f5-118">-Tag</span></span>
<span data-ttu-id="336f5-119">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="336f5-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="336f5-120">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="336f5-120">For example:</span></span>

<span data-ttu-id="336f5-121">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="336f5-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="336f5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="336f5-122">-Confirm</span></span>
<span data-ttu-id="336f5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="336f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336f5-124">-WhatIf</span></span>
<span data-ttu-id="336f5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="336f5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="336f5-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="336f5-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="336f5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="336f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336f5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336f5-128">-DefaultProfile</span></span>
<span data-ttu-id="336f5-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="336f5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="336f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336f5-130">CommonParameters</span></span>
<span data-ttu-id="336f5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="336f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336f5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336f5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="336f5-133">INPUTS</span></span>

### <span data-ttu-id="336f5-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="336f5-134">None</span></span>
<span data-ttu-id="336f5-135">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="336f5-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="336f5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="336f5-136">OUTPUTS</span></span>

### <span data-ttu-id="336f5-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="336f5-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="336f5-138">Bu cmdlet, yeni DNS bölgesini temsil eden bir Microsoft. Azure. Commands. DNS. DnsZone nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="336f5-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="336f5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="336f5-139">NOTES</span></span>
<span data-ttu-id="336f5-140">*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.</span><span class="sxs-lookup"><span data-stu-id="336f5-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="336f5-141">Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.</span><span class="sxs-lookup"><span data-stu-id="336f5-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="336f5-142">*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="336f5-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="336f5-143">*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="336f5-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="336f5-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="336f5-144">RELATED LINKS</span></span>

[<span data-ttu-id="336f5-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="336f5-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="336f5-146">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="336f5-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="336f5-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="336f5-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
