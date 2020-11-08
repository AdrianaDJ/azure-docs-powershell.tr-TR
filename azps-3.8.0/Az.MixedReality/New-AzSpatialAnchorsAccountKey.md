---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 40efd6329b3e4c30df05613b0aa4c5ed738c425c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098863"
---
# <span data-ttu-id="022d3-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="022d3-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="022d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="022d3-102">SYNOPSIS</span></span>
<span data-ttu-id="022d3-103">Uzamsal bağlayıcı hesabının anahtarı</span><span class="sxs-lookup"><span data-stu-id="022d3-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="022d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="022d3-104">SYNTAX</span></span>

### <span data-ttu-id="022d3-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022d3-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022d3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022d3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022d3-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022d3-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="022d3-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="022d3-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="022d3-111">DESCRIPTION</span></span>
<span data-ttu-id="022d3-112">Birincil anahtarı veya ikincil uzamsal bağlayıcı hesabının yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="022d3-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="022d3-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="022d3-113">EXAMPLES</span></span>

### <span data-ttu-id="022d3-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="022d3-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="022d3-115">"RG1" kaynak grubunda uzamsal bağlayıcı hesabının ikincil anahtarını yeniden üret "örnek".</span><span class="sxs-lookup"><span data-stu-id="022d3-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="022d3-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="022d3-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="022d3-117">Geçerli aboneliğin ve "RG1" kaynak grubundan yöneltme ile "örnek" uzamsal bağlayıcı hesabının ikincil anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="022d3-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="022d3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="022d3-118">PARAMETERS</span></span>

### <span data-ttu-id="022d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022d3-119">-DefaultProfile</span></span>
<span data-ttu-id="022d3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="022d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="022d3-121">-Force</span></span>
<span data-ttu-id="022d3-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="022d3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="022d3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="022d3-123">-InputObject</span></span>
<span data-ttu-id="022d3-124">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="022d3-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="022d3-125">-Name</span></span>
<span data-ttu-id="022d3-126">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="022d3-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="022d3-127">-Primary</span></span>
<span data-ttu-id="022d3-128">Uzamsal bağlayıcı hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="022d3-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="022d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="022d3-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="022d3-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="022d3-131">-ResourceId</span></span>
<span data-ttu-id="022d3-132">Uzamsal bağlayıcı hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="022d3-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-133">-İkincil</span><span class="sxs-lookup"><span data-stu-id="022d3-133">-Secondary</span></span>
<span data-ttu-id="022d3-134">Uzamsal bağlayıcı hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="022d3-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022d3-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="022d3-135">-Confirm</span></span>
<span data-ttu-id="022d3-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="022d3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="022d3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="022d3-137">-WhatIf</span></span>
<span data-ttu-id="022d3-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="022d3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="022d3-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="022d3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="022d3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022d3-140">CommonParameters</span></span>
<span data-ttu-id="022d3-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="022d3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="022d3-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022d3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022d3-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="022d3-143">INPUTS</span></span>

### <span data-ttu-id="022d3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="022d3-144">System.String</span></span>

### <span data-ttu-id="022d3-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="022d3-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="022d3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="022d3-146">OUTPUTS</span></span>

### <span data-ttu-id="022d3-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="022d3-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="022d3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="022d3-148">NOTES</span></span>

## <span data-ttu-id="022d3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="022d3-149">RELATED LINKS</span></span>
