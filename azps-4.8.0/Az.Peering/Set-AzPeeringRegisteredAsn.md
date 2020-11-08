---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274719"
---
# <span data-ttu-id="0ad54-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="0ad54-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0ad54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad54-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad54-103">Üst eşleme kaynağından kaydedilen bir ASN 'yi ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ad54-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="0ad54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ad54-104">SYNTAX</span></span>

### <span data-ttu-id="0ad54-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ad54-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad54-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad54-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad54-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0ad54-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad54-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ad54-108">DESCRIPTION</span></span>
<span data-ttu-id="0ad54-109">Üst eşleme kaynağından kaydedilen bir ASN güncelleştirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0ad54-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="0ad54-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ad54-110">EXAMPLES</span></span>

### <span data-ttu-id="0ad54-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ad54-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="0ad54-112">Kimliği kaynak kimliğiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0ad54-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="0ad54-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ad54-113">PARAMETERS</span></span>

### <span data-ttu-id="0ad54-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0ad54-114">-AsJob</span></span>
<span data-ttu-id="0ad54-115">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="0ad54-115">Run in the background.</span></span>

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

### <span data-ttu-id="0ad54-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="0ad54-116">-Asn</span></span>
<span data-ttu-id="0ad54-117">Kaydedilecek ASN</span><span class="sxs-lookup"><span data-stu-id="0ad54-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="0ad54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad54-118">-DefaultProfile</span></span>
<span data-ttu-id="0ad54-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ad54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad54-120">-InputObject</span></span>
<span data-ttu-id="0ad54-121">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="0ad54-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad54-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ad54-122">-Name</span></span>
<span data-ttu-id="0ad54-123">Kaydedilecek ASN</span><span class="sxs-lookup"><span data-stu-id="0ad54-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad54-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="0ad54-124">-PeeringName</span></span>
<span data-ttu-id="0ad54-125">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0ad54-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="0ad54-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad54-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ad54-127">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="0ad54-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="0ad54-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0ad54-128">-ResourceId</span></span>
<span data-ttu-id="0ad54-129">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="0ad54-129">The resource id string name.</span></span>

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

### <span data-ttu-id="0ad54-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ad54-130">-Confirm</span></span>
<span data-ttu-id="0ad54-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ad54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad54-132">-WhatIf</span></span>
<span data-ttu-id="0ad54-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ad54-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad54-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ad54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad54-135">CommonParameters</span></span>
<span data-ttu-id="0ad54-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ad54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad54-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ad54-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad54-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ad54-138">INPUTS</span></span>

### <span data-ttu-id="0ad54-139">Microsoft. Azure. PowerShell. cmdlet. eşleme. modeller. Pspeeringkayıt Teredasn</span><span class="sxs-lookup"><span data-stu-id="0ad54-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="0ad54-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad54-140">System.String</span></span>

## <span data-ttu-id="0ad54-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ad54-141">OUTPUTS</span></span>

### <span data-ttu-id="0ad54-142">Microsoft. Azure. PowerShell. cmdlet. eşleme. modeller. Pspeeringkayıt Teredasn</span><span class="sxs-lookup"><span data-stu-id="0ad54-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0ad54-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ad54-143">NOTES</span></span>

## <span data-ttu-id="0ad54-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ad54-144">RELATED LINKS</span></span>
