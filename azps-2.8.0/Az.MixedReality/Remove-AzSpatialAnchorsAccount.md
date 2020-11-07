---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d164e08876b5489ec45ce146f4f3c7cee3ee6d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751362"
---
# <span data-ttu-id="18b7b-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="18b7b-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="18b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="18b7b-103">Uzamsal bağlayıcı hesabını silme</span><span class="sxs-lookup"><span data-stu-id="18b7b-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="18b7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18b7b-104">SYNTAX</span></span>

### <span data-ttu-id="18b7b-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18b7b-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b7b-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="18b7b-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b7b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="18b7b-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b7b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="18b7b-109">Belirtilen uzamsal Tutturucuların hesabını belirli bir abonelikten ve kaynak grubundan silin.</span><span class="sxs-lookup"><span data-stu-id="18b7b-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="18b7b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18b7b-110">EXAMPLES</span></span>

### <span data-ttu-id="18b7b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18b7b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="18b7b-112">Geçerli abonelikteki ("RG1") uzamsal bağlayıcı hesabını "örnek" olarak silin.</span><span class="sxs-lookup"><span data-stu-id="18b7b-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="18b7b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18b7b-113">PARAMETERS</span></span>

### <span data-ttu-id="18b7b-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="18b7b-114">-Confirm</span></span>
<span data-ttu-id="18b7b-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18b7b-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b7b-116">-DefaultProfile</span></span>
<span data-ttu-id="18b7b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18b7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b7b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b7b-118">-InputObject</span></span>
<span data-ttu-id="18b7b-119">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="18b7b-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="18b7b-120">-Name</span></span>
<span data-ttu-id="18b7b-121">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="18b7b-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="18b7b-122">-PassThru</span></span>
<span data-ttu-id="18b7b-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="18b7b-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="18b7b-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="18b7b-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="18b7b-126">-ResourceId</span></span>
<span data-ttu-id="18b7b-127">Uzamsal bağlayıcı hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="18b7b-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b7b-128">-WhatIf</span></span>
<span data-ttu-id="18b7b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18b7b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b7b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18b7b-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b7b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b7b-131">CommonParameters</span></span>
<span data-ttu-id="18b7b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18b7b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18b7b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b7b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b7b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18b7b-134">INPUTS</span></span>

### <span data-ttu-id="18b7b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="18b7b-135">System.String</span></span>

### <span data-ttu-id="18b7b-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="18b7b-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="18b7b-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18b7b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18b7b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18b7b-138">OUTPUTS</span></span>

### <span data-ttu-id="18b7b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18b7b-139">System.Boolean</span></span>

## <span data-ttu-id="18b7b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18b7b-140">NOTES</span></span>

## <span data-ttu-id="18b7b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18b7b-141">RELATED LINKS</span></span>