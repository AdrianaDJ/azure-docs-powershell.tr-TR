---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 363a6ea9cc6b53ca0c8a75fd32db5222e332bc98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935930"
---
# <span data-ttu-id="5483b-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5483b-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5483b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5483b-102">SYNOPSIS</span></span>
<span data-ttu-id="5483b-103">Cihazda varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5483b-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="5483b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5483b-104">SYNTAX</span></span>

### <span data-ttu-id="5483b-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5483b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5483b-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5483b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5483b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5483b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5483b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5483b-108">DESCRIPTION</span></span>
<span data-ttu-id="5483b-109">**Remove-AzDataBoxEdgeTrigger** cmdlet 'ı, veri kutusu Edge cihazında varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5483b-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="5483b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5483b-110">EXAMPLES</span></span>

### <span data-ttu-id="5483b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5483b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="5483b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5483b-112">PARAMETERS</span></span>

### <span data-ttu-id="5483b-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5483b-113">-AsJob</span></span>
<span data-ttu-id="5483b-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5483b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5483b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5483b-115">-DefaultProfile</span></span>
<span data-ttu-id="5483b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5483b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5483b-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="5483b-117">-DeviceName</span></span>
<span data-ttu-id="5483b-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="5483b-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5483b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5483b-119">-InputObject</span></span>
<span data-ttu-id="5483b-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="5483b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5483b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5483b-121">-Name</span></span>
<span data-ttu-id="5483b-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="5483b-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5483b-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5483b-123">-PassThru</span></span>
<span data-ttu-id="5483b-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="5483b-124">returns true if successful</span></span>

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

### <span data-ttu-id="5483b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5483b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5483b-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5483b-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5483b-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5483b-127">-ResourceId</span></span>
<span data-ttu-id="5483b-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5483b-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5483b-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5483b-129">-Confirm</span></span>
<span data-ttu-id="5483b-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5483b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5483b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5483b-131">-WhatIf</span></span>
<span data-ttu-id="5483b-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5483b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5483b-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5483b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5483b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5483b-134">CommonParameters</span></span>
<span data-ttu-id="5483b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5483b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5483b-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5483b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5483b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5483b-137">INPUTS</span></span>

### <span data-ttu-id="5483b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5483b-138">System.String</span></span>

### <span data-ttu-id="5483b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5483b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5483b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5483b-140">OUTPUTS</span></span>

### <span data-ttu-id="5483b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5483b-141">System.Boolean</span></span>

## <span data-ttu-id="5483b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5483b-142">NOTES</span></span>

## <span data-ttu-id="5483b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5483b-143">RELATED LINKS</span></span>
