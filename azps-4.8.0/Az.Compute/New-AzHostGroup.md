---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109121"
---
# <span data-ttu-id="11053-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="11053-101">New-AzHostGroup</span></span>

## <span data-ttu-id="11053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11053-102">SYNOPSIS</span></span>
<span data-ttu-id="11053-103">Konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11053-103">Creates a host group.</span></span>

## <span data-ttu-id="11053-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11053-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11053-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11053-105">DESCRIPTION</span></span>
<span data-ttu-id="11053-106">Bu cmdlet bir konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11053-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="11053-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11053-107">EXAMPLES</span></span>

### <span data-ttu-id="11053-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11053-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="11053-109">Bu komut, verilen konum ve bölgede bir konak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11053-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="11053-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11053-110">PARAMETERS</span></span>

### <span data-ttu-id="11053-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="11053-111">-AsJob</span></span>
<span data-ttu-id="11053-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="11053-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11053-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11053-113">-DefaultProfile</span></span>
<span data-ttu-id="11053-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11053-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11053-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="11053-115">-Location</span></span>
<span data-ttu-id="11053-116">Konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="11053-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11053-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="11053-117">-Name</span></span>
<span data-ttu-id="11053-118">Konak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11053-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11053-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="11053-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="11053-120">Konak grubunun yayılacağı hata etki alanlarının sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11053-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="11053-121">En küçük değer 1 ve en yüksek değer 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="11053-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11053-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11053-122">-ResourceGroupName</span></span>
<span data-ttu-id="11053-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="11053-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11053-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="11053-124">-Tag</span></span>
<span data-ttu-id="11053-125">Etiketleri belirtir</span><span class="sxs-lookup"><span data-stu-id="11053-125">Specifies Tags</span></span>

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

### <span data-ttu-id="11053-126">-Bölge</span><span class="sxs-lookup"><span data-stu-id="11053-126">-Zone</span></span>
<span data-ttu-id="11053-127">Konak grubunun bölgelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="11053-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11053-128">-Supportautomaticyerleştirmesini</span><span class="sxs-lookup"><span data-stu-id="11053-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="11053-129">HostGroup 'un VM 'nin otomatik yerleştirmesini etkinleştirip etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="11053-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="11053-130">Otomatik yerleştirme, bu VM 'Ler adanmış ana bilgisayar grubu altında Azure tarafından seçilen adanmış ana bilgisayarlara yerleştirilirler.</span><span class="sxs-lookup"><span data-stu-id="11053-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="11053-131">Belirtilmezse, varsayılan değer doğru olacaktır.</span><span class="sxs-lookup"><span data-stu-id="11053-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="11053-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="11053-132">-Confirm</span></span>
<span data-ttu-id="11053-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11053-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11053-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11053-134">-WhatIf</span></span>
<span data-ttu-id="11053-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11053-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11053-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11053-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11053-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11053-137">CommonParameters</span></span>
<span data-ttu-id="11053-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11053-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11053-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="11053-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11053-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11053-140">INPUTS</span></span>

### <span data-ttu-id="11053-141">System. String</span><span class="sxs-lookup"><span data-stu-id="11053-141">System.String</span></span>

## <span data-ttu-id="11053-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11053-142">OUTPUTS</span></span>

### <span data-ttu-id="11053-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="11053-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="11053-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11053-144">NOTES</span></span>

## <span data-ttu-id="11053-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11053-145">RELATED LINKS</span></span>
