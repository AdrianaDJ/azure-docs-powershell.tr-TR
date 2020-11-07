---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 043b97a256fff50ca9831685a90f0cfb46ff7277
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915724"
---
# <span data-ttu-id="aaf0b-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="aaf0b-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="aaf0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf0b-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf0b-103">Uzamsal bağlayıcı hesabının anahtarı</span><span class="sxs-lookup"><span data-stu-id="aaf0b-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="aaf0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aaf0b-104">SYNTAX</span></span>

### <span data-ttu-id="aaf0b-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf0b-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf0b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf0b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf0b-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf0b-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf0b-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaf0b-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="aaf0b-111">DESCRIPTION</span></span>
<span data-ttu-id="aaf0b-112">Renegrate birincil anahtarı veya</span><span class="sxs-lookup"><span data-stu-id="aaf0b-112">Renegrate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="aaf0b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aaf0b-113">EXAMPLES</span></span>

### <span data-ttu-id="aaf0b-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aaf0b-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="aaf0b-115">"RG1" kaynak grubunda uzamsal bağlayıcı hesabının ikincil anahtarını yeniden üret "örnek".</span><span class="sxs-lookup"><span data-stu-id="aaf0b-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="aaf0b-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aaf0b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="aaf0b-117">Geçerli aboneliğin ve "RG1" kaynak grubundan yöneltme ile "örnek" uzamsal bağlayıcı hesabının ikincil anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="aaf0b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aaf0b-118">PARAMETERS</span></span>

### <span data-ttu-id="aaf0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf0b-119">-DefaultProfile</span></span>
<span data-ttu-id="aaf0b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf0b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aaf0b-121">-Force</span></span>
<span data-ttu-id="aaf0b-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aaf0b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf0b-123">-InputObject</span></span>
<span data-ttu-id="aaf0b-124">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-124">The custom domain object.</span></span>

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

### <span data-ttu-id="aaf0b-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="aaf0b-125">-Name</span></span>
<span data-ttu-id="aaf0b-126">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="aaf0b-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="aaf0b-127">-Primary</span></span>
<span data-ttu-id="aaf0b-128">Uzamsal bağlayıcı hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="aaf0b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf0b-129">-ResourceGroupName</span></span>
<span data-ttu-id="aaf0b-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="aaf0b-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aaf0b-131">-ResourceId</span></span>
<span data-ttu-id="aaf0b-132">Uzamsal bağlayıcı hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="aaf0b-133">-İkincil</span><span class="sxs-lookup"><span data-stu-id="aaf0b-133">-Secondary</span></span>
<span data-ttu-id="aaf0b-134">Uzamsal bağlayıcı hesabının birincil anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="aaf0b-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="aaf0b-135">-Confirm</span></span>
<span data-ttu-id="aaf0b-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf0b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf0b-137">-WhatIf</span></span>
<span data-ttu-id="aaf0b-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaf0b-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf0b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf0b-140">CommonParameters</span></span>
<span data-ttu-id="aaf0b-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aaf0b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aaf0b-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf0b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf0b-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aaf0b-143">INPUTS</span></span>

### <span data-ttu-id="aaf0b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aaf0b-144">System.String</span></span>

### <span data-ttu-id="aaf0b-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="aaf0b-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="aaf0b-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aaf0b-146">OUTPUTS</span></span>

### <span data-ttu-id="aaf0b-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aaf0b-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="aaf0b-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aaf0b-148">NOTES</span></span>

## <span data-ttu-id="aaf0b-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aaf0b-149">RELATED LINKS</span></span>
