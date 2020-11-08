---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275644"
---
# <span data-ttu-id="d558a-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d558a-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d558a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d558a-102">SYNOPSIS</span></span>
<span data-ttu-id="d558a-103">Bir kullanılabilirlik grubu dinleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="d558a-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="d558a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d558a-104">SYNTAX</span></span>

### <span data-ttu-id="d558a-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d558a-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d558a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d558a-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d558a-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d558a-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d558a-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="d558a-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d558a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d558a-109">DESCRIPTION</span></span>
<span data-ttu-id="d558a-110">Remove-AzAvailabilityGroupListener cmdlet 'i bir kullanılabilirlik grubu dinleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="d558a-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="d558a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d558a-111">EXAMPLES</span></span>

### <span data-ttu-id="d558a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d558a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="d558a-113">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="d558a-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d558a-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d558a-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d558a-115">AgListener01 kullanılabilirlik grubundaki kullanılabilirlik grubu dinleyicisi 'ni siler.</span><span class="sxs-lookup"><span data-stu-id="d558a-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="d558a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d558a-116">PARAMETERS</span></span>

### <span data-ttu-id="d558a-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="d558a-117">-AsJob</span></span>
<span data-ttu-id="d558a-118">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d558a-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d558a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d558a-119">-DefaultProfile</span></span>
<span data-ttu-id="d558a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d558a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d558a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d558a-121">-InputObject</span></span>
<span data-ttu-id="d558a-122">Kullanılabilirlik grubu dinleyici nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d558a-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d558a-123">-Name</span></span>
<span data-ttu-id="d558a-124">Kullanılabilirlik grubu dinleyicisi adı.</span><span class="sxs-lookup"><span data-stu-id="d558a-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d558a-125">-PassThru</span></span>
<span data-ttu-id="d558a-126">, Cmdlet 'in yürütülmesinin sonunda silinen kaynağın çıktısının mi edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d558a-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="d558a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d558a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d558a-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d558a-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d558a-129">-ResourceId</span></span>
<span data-ttu-id="d558a-130">Kullanılabilirlik grubu dinleyicisi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d558a-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="d558a-131">-SqlVMGroupName</span></span>
<span data-ttu-id="d558a-132">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d558a-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="d558a-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="d558a-134">SQL sanal makine grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d558a-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d558a-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="d558a-135">-Confirm</span></span>
<span data-ttu-id="d558a-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d558a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d558a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d558a-137">-WhatIf</span></span>
<span data-ttu-id="d558a-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d558a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d558a-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d558a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d558a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d558a-140">CommonParameters</span></span>
<span data-ttu-id="d558a-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d558a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d558a-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d558a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d558a-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d558a-143">INPUTS</span></span>

### <span data-ttu-id="d558a-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d558a-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="d558a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d558a-145">System.String</span></span>

### <span data-ttu-id="d558a-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="d558a-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d558a-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d558a-147">OUTPUTS</span></span>

### <span data-ttu-id="d558a-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d558a-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d558a-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d558a-149">NOTES</span></span>

## <span data-ttu-id="d558a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d558a-150">RELATED LINKS</span></span>
