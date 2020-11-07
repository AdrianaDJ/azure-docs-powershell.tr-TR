---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937932"
---
# <span data-ttu-id="3c006-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3c006-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3c006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c006-102">SYNOPSIS</span></span>
<span data-ttu-id="3c006-103">SQL sanal makine grubunda bir veya daha fazla kullanılabilirlik grubu dinleyicilerini alın.</span><span class="sxs-lookup"><span data-stu-id="3c006-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3c006-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c006-104">SYNTAX</span></span>

### <span data-ttu-id="3c006-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c006-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c006-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3c006-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c006-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3c006-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c006-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c006-108">DESCRIPTION</span></span>
<span data-ttu-id="3c006-109">Get-AzAvailabilityGroupListener SQL sanal makine grubundan bir veya daha fazla kullanılabilirlik grubu dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="3c006-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3c006-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c006-110">EXAMPLES</span></span>

### <span data-ttu-id="3c006-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c006-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="3c006-112">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="3c006-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c006-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c006-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3c006-114">Bu komut, SQL sanal makine AgListener01 SqlVmGroup01 ve kaynak grubu ResourceGroup01 kullanılabilirlik grubu dinleyicisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3c006-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3c006-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3c006-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="3c006-116">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="3c006-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c006-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c006-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3c006-118">Bu komut, SQL sanal makine SqlVmGroup01 ve kaynak grubu ResourceGroup01 tüm kullanılabilirlik grubu dinleyicileri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3c006-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3c006-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3c006-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="3c006-120">Name ResourceGroupName Grupadi Bilitygroupname</span><span class="sxs-lookup"><span data-stu-id="3c006-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3c006-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3c006-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="3c006-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c006-122">PARAMETERS</span></span>

### <span data-ttu-id="3c006-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c006-123">-DefaultProfile</span></span>
<span data-ttu-id="3c006-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c006-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c006-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c006-125">-Name</span></span>
<span data-ttu-id="3c006-126">Kullanılabilirlik grubu dinleyicisi adı.</span><span class="sxs-lookup"><span data-stu-id="3c006-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c006-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c006-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c006-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3c006-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c006-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3c006-129">-ResourceId</span></span>
<span data-ttu-id="3c006-130">Kullanılabilirlik grubu dinleyicisi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3c006-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="3c006-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3c006-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3c006-132">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3c006-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="3c006-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3c006-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3c006-134">SQL sanal makine grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3c006-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="3c006-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c006-135">CommonParameters</span></span>
<span data-ttu-id="3c006-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c006-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c006-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c006-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c006-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c006-138">INPUTS</span></span>

### <span data-ttu-id="3c006-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3c006-139">System.String</span></span>

### <span data-ttu-id="3c006-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="3c006-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3c006-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c006-141">OUTPUTS</span></span>

### <span data-ttu-id="3c006-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3c006-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3c006-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c006-143">NOTES</span></span>

## <span data-ttu-id="3c006-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c006-144">RELATED LINKS</span></span>
