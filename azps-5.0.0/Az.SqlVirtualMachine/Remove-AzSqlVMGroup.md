---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275642"
---
# <span data-ttu-id="50433-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="50433-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="50433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50433-102">SYNOPSIS</span></span>
<span data-ttu-id="50433-103">SQL sanal makine grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="50433-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="50433-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50433-104">SYNTAX</span></span>

### <span data-ttu-id="50433-105">ParamaterList (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50433-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50433-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50433-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50433-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="50433-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50433-108">Adlandır</span><span class="sxs-lookup"><span data-stu-id="50433-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50433-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="50433-109">DESCRIPTION</span></span>
<span data-ttu-id="50433-110">Remove-AzSqlVMGroup cmdlet 'i bir SQL sanal makine grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="50433-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="50433-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50433-111">EXAMPLES</span></span>

### <span data-ttu-id="50433-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="50433-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="50433-113">Kaynak grubundaki ResourceGroup01 Azure SQL sanal makine grubunu (test grubu) siler.</span><span class="sxs-lookup"><span data-stu-id="50433-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="50433-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50433-114">PARAMETERS</span></span>

### <span data-ttu-id="50433-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="50433-115">-AsJob</span></span>
<span data-ttu-id="50433-116">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="50433-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="50433-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50433-117">-DefaultProfile</span></span>
<span data-ttu-id="50433-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50433-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50433-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50433-119">-InputObject</span></span>
<span data-ttu-id="50433-120">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="50433-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50433-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="50433-121">-Name</span></span>
<span data-ttu-id="50433-122">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="50433-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50433-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="50433-123">-PassThru</span></span>
<span data-ttu-id="50433-124">, Cmdlet 'in yürütülmesinin sonunda silinen kaynağın çıktısının mi edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50433-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="50433-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50433-125">-ResourceGroupName</span></span>
<span data-ttu-id="50433-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="50433-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="50433-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="50433-127">-ResourceId</span></span>
<span data-ttu-id="50433-128">SQL sanal makine grubu kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="50433-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50433-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="50433-129">-Confirm</span></span>
<span data-ttu-id="50433-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50433-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50433-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50433-131">-WhatIf</span></span>
<span data-ttu-id="50433-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50433-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50433-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50433-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50433-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50433-134">CommonParameters</span></span>
<span data-ttu-id="50433-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50433-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50433-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50433-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50433-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50433-137">INPUTS</span></span>

### <span data-ttu-id="50433-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="50433-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="50433-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50433-139">System.String</span></span>

## <span data-ttu-id="50433-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50433-140">OUTPUTS</span></span>

### <span data-ttu-id="50433-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="50433-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="50433-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50433-142">NOTES</span></span>

## <span data-ttu-id="50433-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50433-143">RELATED LINKS</span></span>
