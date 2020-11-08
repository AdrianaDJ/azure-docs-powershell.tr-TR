---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098560"
---
# <span data-ttu-id="7b770-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7b770-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="7b770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b770-102">SYNOPSIS</span></span>
<span data-ttu-id="7b770-103">Yeni bir özel DNS bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b770-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="7b770-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b770-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b770-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b770-105">DESCRIPTION</span></span>
<span data-ttu-id="7b770-106">**New-AzPrivateDnsZone** cmdlet 'i belirtilen kaynak grubunda yeni bir özel etki alanı adı SISTEMI (DNS) bölgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b770-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="7b770-107">*Name* parametresi için benzersiz BIR özel DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="7b770-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="7b770-108">Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzPrivateDnsRecordSet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b770-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="7b770-109">Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b770-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7b770-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b770-110">EXAMPLES</span></span>

### <span data-ttu-id="7b770-111">Örnek 1: özel bir DNS bölgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7b770-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="7b770-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b770-112">PARAMETERS</span></span>

### <span data-ttu-id="7b770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b770-113">-DefaultProfile</span></span>
<span data-ttu-id="7b770-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7b770-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b770-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b770-115">-Name</span></span>
<span data-ttu-id="7b770-116">Oluşturulacak özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b770-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="7b770-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b770-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b770-118">Bölgenin oluşturulacağı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b770-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="7b770-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7b770-119">-Tag</span></span>
<span data-ttu-id="7b770-120">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="7b770-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b770-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b770-121">-Confirm</span></span>
<span data-ttu-id="7b770-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b770-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b770-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b770-123">-WhatIf</span></span>
<span data-ttu-id="7b770-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b770-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b770-125">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b770-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b770-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b770-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b770-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b770-127">CommonParameters</span></span>
<span data-ttu-id="7b770-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b770-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b770-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b770-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b770-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b770-130">INPUTS</span></span>

### <span data-ttu-id="7b770-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7b770-131">None</span></span>

## <span data-ttu-id="7b770-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b770-132">OUTPUTS</span></span>

### <span data-ttu-id="7b770-133">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7b770-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="7b770-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b770-134">NOTES</span></span>

## <span data-ttu-id="7b770-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b770-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b770-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7b770-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="7b770-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7b770-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="7b770-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7b770-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)