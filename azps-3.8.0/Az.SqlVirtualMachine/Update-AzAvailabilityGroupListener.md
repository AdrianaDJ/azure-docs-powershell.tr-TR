---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098096"
---
# <span data-ttu-id="1af38-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="1af38-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="1af38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af38-102">SYNOPSIS</span></span>
<span data-ttu-id="1af38-103">Kullanılabilirlik grubu dinleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1af38-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="1af38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1af38-104">SYNTAX</span></span>

### <span data-ttu-id="1af38-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1af38-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1af38-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1af38-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1af38-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1af38-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af38-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="1af38-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af38-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1af38-109">DESCRIPTION</span></span>
<span data-ttu-id="1af38-110">Update-AzAvailabilityGroupListener cmdlet 'i bir kullanılabilirlik grubu dinleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1af38-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="1af38-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1af38-111">EXAMPLES</span></span>

### <span data-ttu-id="1af38-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1af38-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="1af38-113">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="1af38-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="1af38-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="1af38-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="1af38-115">Kullanılabilirlik grubu dinleyicisi için liste SQL sanal makinelerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1af38-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="1af38-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1af38-116">PARAMETERS</span></span>

### <span data-ttu-id="1af38-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="1af38-117">-AsJob</span></span>
<span data-ttu-id="1af38-118">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1af38-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1af38-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af38-119">-DefaultProfile</span></span>
<span data-ttu-id="1af38-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1af38-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af38-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af38-121">-InputObject</span></span>
<span data-ttu-id="1af38-122">Kullanılabilirlik grubu dinleyici nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1af38-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="1af38-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1af38-123">-Name</span></span>
<span data-ttu-id="1af38-124">Kullanılabilirlik grubu dinleyicisi adı.</span><span class="sxs-lookup"><span data-stu-id="1af38-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="1af38-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af38-125">-ResourceGroupName</span></span>
<span data-ttu-id="1af38-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1af38-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1af38-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1af38-127">-ResourceId</span></span>
<span data-ttu-id="1af38-128">Kullanılabilirlik grubu dinleyicisi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1af38-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af38-129">-Sqlvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="1af38-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="1af38-130">SQL VM kaynak kimliklerinin listesi</span><span class="sxs-lookup"><span data-stu-id="1af38-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af38-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="1af38-131">-SqlVMGroupName</span></span>
<span data-ttu-id="1af38-132">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1af38-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="1af38-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="1af38-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="1af38-134">SQL sanal makine grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1af38-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="1af38-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="1af38-135">-Confirm</span></span>
<span data-ttu-id="1af38-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1af38-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af38-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af38-137">-WhatIf</span></span>
<span data-ttu-id="1af38-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1af38-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af38-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1af38-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af38-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af38-140">CommonParameters</span></span>
<span data-ttu-id="1af38-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1af38-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af38-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1af38-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af38-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1af38-143">INPUTS</span></span>

### <span data-ttu-id="1af38-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="1af38-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="1af38-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1af38-145">System.String</span></span>

### <span data-ttu-id="1af38-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="1af38-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="1af38-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1af38-147">OUTPUTS</span></span>

### <span data-ttu-id="1af38-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="1af38-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="1af38-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1af38-149">NOTES</span></span>

## <span data-ttu-id="1af38-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1af38-150">RELATED LINKS</span></span>
