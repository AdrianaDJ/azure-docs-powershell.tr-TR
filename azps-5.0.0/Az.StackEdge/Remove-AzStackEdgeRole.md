---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278775"
---
# <span data-ttu-id="776d3-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="776d3-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="776d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="776d3-102">SYNOPSIS</span></span>
<span data-ttu-id="776d3-103">Aygıtın ilişkili IoT rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="776d3-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="776d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="776d3-104">SYNTAX</span></span>

### <span data-ttu-id="776d3-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="776d3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776d3-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="776d3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776d3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="776d3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="776d3-108">DESCRIPTION</span></span>
<span data-ttu-id="776d3-109">**Remove-AzStackEdgeRole** cmdlet 'ı, yığın uç aygıtının ilişkili IoT rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="776d3-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="776d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="776d3-110">EXAMPLES</span></span>

### <span data-ttu-id="776d3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="776d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="776d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="776d3-112">PARAMETERS</span></span>

### <span data-ttu-id="776d3-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="776d3-113">-AsJob</span></span>
<span data-ttu-id="776d3-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="776d3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="776d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776d3-115">-DefaultProfile</span></span>
<span data-ttu-id="776d3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="776d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="776d3-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="776d3-117">-DeviceName</span></span>
<span data-ttu-id="776d3-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="776d3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="776d3-119">-InputObject</span></span>
<span data-ttu-id="776d3-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="776d3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="776d3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="776d3-121">-Name</span></span>
<span data-ttu-id="776d3-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="776d3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d3-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="776d3-123">-PassThru</span></span>
<span data-ttu-id="776d3-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="776d3-124">returns true if successful</span></span>

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

### <span data-ttu-id="776d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="776d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="776d3-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="776d3-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d3-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="776d3-127">-ResourceId</span></span>
<span data-ttu-id="776d3-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="776d3-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776d3-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="776d3-129">-Confirm</span></span>
<span data-ttu-id="776d3-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="776d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776d3-131">-WhatIf</span></span>
<span data-ttu-id="776d3-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="776d3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="776d3-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="776d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776d3-134">CommonParameters</span></span>
<span data-ttu-id="776d3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="776d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776d3-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="776d3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776d3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="776d3-137">INPUTS</span></span>

### <span data-ttu-id="776d3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="776d3-138">System.String</span></span>

### <span data-ttu-id="776d3-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="776d3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="776d3-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="776d3-140">OUTPUTS</span></span>

### <span data-ttu-id="776d3-141">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="776d3-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="776d3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="776d3-142">NOTES</span></span>

## <span data-ttu-id="776d3-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="776d3-143">RELATED LINKS</span></span>
