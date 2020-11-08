---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277217"
---
# <span data-ttu-id="816d9-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="816d9-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="816d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="816d9-102">SYNOPSIS</span></span>
<span data-ttu-id="816d9-103">Eşleme için tescilli ASN oluşturma</span><span class="sxs-lookup"><span data-stu-id="816d9-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="816d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="816d9-104">SYNTAX</span></span>

### <span data-ttu-id="816d9-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="816d9-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816d9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="816d9-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816d9-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="816d9-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="816d9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="816d9-108">DESCRIPTION</span></span>
<span data-ttu-id="816d9-109">Eşleme nesneleri için kaydedilmiş ASNs oluşturma.</span><span class="sxs-lookup"><span data-stu-id="816d9-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="816d9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="816d9-110">EXAMPLES</span></span>

### <span data-ttu-id="816d9-111">Eşleme alma ve kaydedilmiş bir ASN oluşturma</span><span class="sxs-lookup"><span data-stu-id="816d9-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="816d9-112">Kaydettirilmiş bir ASN eklemek istediğiniz eşlemeyi edinin.</span><span class="sxs-lookup"><span data-stu-id="816d9-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="816d9-113">Ardından bunu commandto 'ya iletin.</span><span class="sxs-lookup"><span data-stu-id="816d9-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="816d9-114">Kaydedilmiş bir ASN oluşturmak için eşleme RESOURCEID kullanma</span><span class="sxs-lookup"><span data-stu-id="816d9-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="816d9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="816d9-115">PARAMETERS</span></span>

### <span data-ttu-id="816d9-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="816d9-116">-AsJob</span></span>
<span data-ttu-id="816d9-117">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="816d9-117">Run in the background.</span></span>

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

### <span data-ttu-id="816d9-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="816d9-118">-Asn</span></span>
<span data-ttu-id="816d9-119">Kaydedilecek ASN</span><span class="sxs-lookup"><span data-stu-id="816d9-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="816d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="816d9-120">-DefaultProfile</span></span>
<span data-ttu-id="816d9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="816d9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="816d9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="816d9-122">-InputObject</span></span>
<span data-ttu-id="816d9-123">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="816d9-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="816d9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="816d9-124">-Name</span></span>
<span data-ttu-id="816d9-125">Kaydedilecek ASN</span><span class="sxs-lookup"><span data-stu-id="816d9-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="816d9-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="816d9-126">-PeeringName</span></span>
<span data-ttu-id="816d9-127">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="816d9-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="816d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="816d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="816d9-129">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="816d9-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="816d9-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="816d9-130">-ResourceId</span></span>
<span data-ttu-id="816d9-131">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="816d9-131">The resource id string name.</span></span>

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

### <span data-ttu-id="816d9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="816d9-132">-Confirm</span></span>
<span data-ttu-id="816d9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="816d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="816d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="816d9-134">-WhatIf</span></span>
<span data-ttu-id="816d9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="816d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="816d9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="816d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="816d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816d9-137">CommonParameters</span></span>
<span data-ttu-id="816d9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="816d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816d9-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="816d9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816d9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="816d9-140">INPUTS</span></span>

### <span data-ttu-id="816d9-141">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="816d9-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="816d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="816d9-142">System.String</span></span>

## <span data-ttu-id="816d9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="816d9-143">OUTPUTS</span></span>

### <span data-ttu-id="816d9-144">Microsoft. Azure. PowerShell. cmdlet. eşleme. modeller. Pspeeringkayıt Teredasn</span><span class="sxs-lookup"><span data-stu-id="816d9-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="816d9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="816d9-145">NOTES</span></span>

## <span data-ttu-id="816d9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="816d9-146">RELATED LINKS</span></span>
