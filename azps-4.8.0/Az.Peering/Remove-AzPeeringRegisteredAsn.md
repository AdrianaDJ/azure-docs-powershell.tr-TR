---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274718"
---
# <span data-ttu-id="0eb70-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="0eb70-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0eb70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb70-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb70-103">Üst eşleme kaynağından kaydedilmiş bir ASN silme veya kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0eb70-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="0eb70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0eb70-104">SYNTAX</span></span>

### <span data-ttu-id="0eb70-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0eb70-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb70-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb70-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0eb70-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb70-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0eb70-108">DESCRIPTION</span></span>
<span data-ttu-id="0eb70-109">Üst eşleme kaynağından kaydedilen ASN 'nin kaldırılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0eb70-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="0eb70-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0eb70-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb70-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0eb70-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="0eb70-112">Kaynak kimliği ile registerd ASN 'i kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0eb70-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="0eb70-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0eb70-113">PARAMETERS</span></span>

### <span data-ttu-id="0eb70-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0eb70-114">-AsJob</span></span>
<span data-ttu-id="0eb70-115">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="0eb70-115">Run in the background.</span></span>

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

### <span data-ttu-id="0eb70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb70-116">-DefaultProfile</span></span>
<span data-ttu-id="0eb70-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0eb70-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb70-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0eb70-118">-Force</span></span>
<span data-ttu-id="0eb70-119">İşlemin tamamlamasını zorunlu kılın</span><span class="sxs-lookup"><span data-stu-id="0eb70-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="0eb70-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb70-120">-InputObject</span></span>
<span data-ttu-id="0eb70-121">Get-AzPeeringServicePrefix kullanma</span><span class="sxs-lookup"><span data-stu-id="0eb70-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb70-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0eb70-122">-Name</span></span>
<span data-ttu-id="0eb70-123">Tescilli ASN 'nin adı</span><span class="sxs-lookup"><span data-stu-id="0eb70-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb70-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0eb70-124">-PassThru</span></span>
<span data-ttu-id="0eb70-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0eb70-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0eb70-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="0eb70-126">-PeeringName</span></span>
<span data-ttu-id="0eb70-127">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0eb70-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb70-128">-ResourceGroupName</span></span>
<span data-ttu-id="0eb70-129">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="0eb70-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb70-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0eb70-130">-ResourceId</span></span>
<span data-ttu-id="0eb70-131">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="0eb70-131">The resource id string name.</span></span>

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

### <span data-ttu-id="0eb70-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0eb70-132">-Confirm</span></span>
<span data-ttu-id="0eb70-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0eb70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb70-134">-WhatIf</span></span>
<span data-ttu-id="0eb70-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0eb70-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb70-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0eb70-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb70-137">CommonParameters</span></span>
<span data-ttu-id="0eb70-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0eb70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb70-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0eb70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb70-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0eb70-140">INPUTS</span></span>

### <span data-ttu-id="0eb70-141">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb70-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="0eb70-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb70-142">System.String</span></span>

## <span data-ttu-id="0eb70-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0eb70-143">OUTPUTS</span></span>

### <span data-ttu-id="0eb70-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0eb70-144">System.Boolean</span></span>

## <span data-ttu-id="0eb70-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0eb70-145">NOTES</span></span>

## <span data-ttu-id="0eb70-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0eb70-146">RELATED LINKS</span></span>
