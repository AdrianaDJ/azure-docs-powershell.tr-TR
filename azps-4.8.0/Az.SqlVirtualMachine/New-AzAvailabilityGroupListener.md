---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107537"
---
# <span data-ttu-id="8a9a4-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="8a9a4-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="8a9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9a4-103">Yeni bir kullanılabilirlik grubu dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="8a9a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a9a4-104">SYNTAX</span></span>

### <span data-ttu-id="8a9a4-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a9a4-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a9a4-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="8a9a4-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a9a4-107">DESCRIPTION</span></span>
<span data-ttu-id="8a9a4-108">New-AzAvailabilityGroupListener cmdlet 'i yeni bir kullanılabilirlik grubu dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="8a9a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a9a4-109">EXAMPLES</span></span>

### <span data-ttu-id="8a9a4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a9a4-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="8a9a4-111">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="8a9a4-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="8a9a4-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="8a9a4-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="8a9a4-113">SQL sanal makine grubunda AvailabilityGroup01 kullanılabilirlik grubu için yeni bir kullanılabilirlik grubu dinleyicisi AgListener01 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="8a9a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a9a4-114">PARAMETERS</span></span>

### <span data-ttu-id="8a9a4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8a9a4-115">-AsJob</span></span>
<span data-ttu-id="8a9a4-116">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8a9a4-117">-Kullanılabilirlik Grupadi</span><span class="sxs-lookup"><span data-stu-id="8a9a4-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="8a9a4-118">Kullanılabilirlik grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9a4-119">-DefaultProfile</span></span>
<span data-ttu-id="8a9a4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9a4-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="8a9a4-121">-IpAddress</span></span>
<span data-ttu-id="8a9a4-122">Özel IP adresi</span><span class="sxs-lookup"><span data-stu-id="8a9a4-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-123">-Loadbalancerresourceıd</span><span class="sxs-lookup"><span data-stu-id="8a9a4-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="8a9a4-124">Yük dengeleyici kimliği</span><span class="sxs-lookup"><span data-stu-id="8a9a4-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a9a4-125">-Name</span></span>
<span data-ttu-id="8a9a4-126">Kullanılabilirlik grubu dinleyicisi adı.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-127">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8a9a4-127">-Port</span></span>
<span data-ttu-id="8a9a4-128">AĞ dinleyicisi bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-128">Port number of AG Listener.</span></span> <span data-ttu-id="8a9a4-129">Varsayılan değer 1433 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="8a9a4-130">-ProbePort</span></span>
<span data-ttu-id="8a9a4-131">Araştırma bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8a9a4-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-132">-Publicıpadresresourceıd</span><span class="sxs-lookup"><span data-stu-id="8a9a4-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="8a9a4-133">Ortak IP adresi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8a9a4-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9a4-134">-ResourceGroupName</span></span>
<span data-ttu-id="8a9a4-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="8a9a4-136">-Sqlvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="8a9a4-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="8a9a4-137">SQL VM kaynak kimliklerinin listesi</span><span class="sxs-lookup"><span data-stu-id="8a9a4-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9a4-138">-SqlVMGroupName</span></span>
<span data-ttu-id="8a9a4-139">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="8a9a4-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="8a9a4-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="8a9a4-141">SQL sanal makine grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="8a9a4-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8a9a4-142">-SubnetId</span></span>
<span data-ttu-id="8a9a4-143">Alt ağ kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8a9a4-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a4-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a9a4-144">-Confirm</span></span>
<span data-ttu-id="8a9a4-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9a4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9a4-146">-WhatIf</span></span>
<span data-ttu-id="8a9a4-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9a4-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9a4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9a4-149">CommonParameters</span></span>
<span data-ttu-id="8a9a4-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9a4-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8a9a4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9a4-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a9a4-152">INPUTS</span></span>

### <span data-ttu-id="8a9a4-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="8a9a4-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8a9a4-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a9a4-154">OUTPUTS</span></span>

### <span data-ttu-id="8a9a4-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="8a9a4-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="8a9a4-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a9a4-156">NOTES</span></span>

## <span data-ttu-id="8a9a4-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a9a4-157">RELATED LINKS</span></span>
