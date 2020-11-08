---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276876"
---
# <span data-ttu-id="60d97-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="60d97-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="60d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60d97-102">SYNOPSIS</span></span>
<span data-ttu-id="60d97-103">Eşleme nesneleri için kaydedilmiş önekler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="60d97-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="60d97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60d97-104">SYNTAX</span></span>

### <span data-ttu-id="60d97-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60d97-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60d97-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="60d97-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60d97-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="60d97-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60d97-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60d97-108">DESCRIPTION</span></span>
<span data-ttu-id="60d97-109">Eşleme nesneleri için kaydedilmiş önekler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="60d97-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="60d97-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60d97-110">EXAMPLES</span></span>

### <span data-ttu-id="60d97-111">Eşleme alma ve kaydedilmiş önek oluşturma</span><span class="sxs-lookup"><span data-stu-id="60d97-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="60d97-112">Kaydettirilmiş bir önek eklemek istediğiniz eşlemeyi edinin.</span><span class="sxs-lookup"><span data-stu-id="60d97-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="60d97-113">Ardından bunu commandto 'ya iletin.</span><span class="sxs-lookup"><span data-stu-id="60d97-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="60d97-114">Kaydedilmiş bir ASN oluşturmak için eşleme RESOURCEID kullanma</span><span class="sxs-lookup"><span data-stu-id="60d97-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="60d97-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60d97-115">PARAMETERS</span></span>

### <span data-ttu-id="60d97-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="60d97-116">-AsJob</span></span>
<span data-ttu-id="60d97-117">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="60d97-117">Run in the background.</span></span>

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

### <span data-ttu-id="60d97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d97-118">-DefaultProfile</span></span>
<span data-ttu-id="60d97-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60d97-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d97-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60d97-120">-InputObject</span></span>
<span data-ttu-id="60d97-121">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="60d97-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60d97-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="60d97-122">-Name</span></span>
<span data-ttu-id="60d97-123">Önek adı.</span><span class="sxs-lookup"><span data-stu-id="60d97-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d97-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="60d97-124">-PeeringName</span></span>
<span data-ttu-id="60d97-125">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="60d97-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d97-126">-Önek</span><span class="sxs-lookup"><span data-stu-id="60d97-126">-Prefix</span></span>
<span data-ttu-id="60d97-127">Oturum IPv4 öneki</span><span class="sxs-lookup"><span data-stu-id="60d97-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="60d97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d97-128">-ResourceGroupName</span></span>
<span data-ttu-id="60d97-129">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="60d97-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d97-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="60d97-130">-ResourceId</span></span>
<span data-ttu-id="60d97-131">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="60d97-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d97-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="60d97-132">-Confirm</span></span>
<span data-ttu-id="60d97-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60d97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d97-134">-WhatIf</span></span>
<span data-ttu-id="60d97-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60d97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60d97-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60d97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d97-137">CommonParameters</span></span>
<span data-ttu-id="60d97-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60d97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d97-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60d97-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d97-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60d97-140">INPUTS</span></span>

### <span data-ttu-id="60d97-141">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d97-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="60d97-142">System. String</span><span class="sxs-lookup"><span data-stu-id="60d97-142">System.String</span></span>

## <span data-ttu-id="60d97-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60d97-143">OUTPUTS</span></span>

### <span data-ttu-id="60d97-144">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d97-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="60d97-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60d97-145">NOTES</span></span>

## <span data-ttu-id="60d97-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60d97-146">RELATED LINKS</span></span>
