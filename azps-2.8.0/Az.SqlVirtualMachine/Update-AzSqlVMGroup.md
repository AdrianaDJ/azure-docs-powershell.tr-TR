---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: ea86c4e0a016ae2b33c7853ba9851762a7d8ca54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933958"
---
# <span data-ttu-id="a0bd3-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="a0bd3-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="a0bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bd3-103">SQL sanal makine grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="a0bd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0bd3-104">SYNTAX</span></span>

### <span data-ttu-id="a0bd3-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0bd3-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bd3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0bd3-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0bd3-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a0bd3-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bd3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="a0bd3-109">Update-AzSqlVMGroup cmdlet 'i bir SQL sanal makine grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="a0bd3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0bd3-110">EXAMPLES</span></span>

### <span data-ttu-id="a0bd3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0bd3-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="a0bd3-112">SQL sanal makine grubunun etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="a0bd3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0bd3-113">PARAMETERS</span></span>

### <span data-ttu-id="a0bd3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a0bd3-114">-AsJob</span></span>
<span data-ttu-id="a0bd3-115">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0bd3-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="a0bd3-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="a0bd3-117">Küme oluştururken kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="a0bd3-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="a0bd3-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="a0bd3-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="a0bd3-119">İşletim kümesi için kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="a0bd3-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="a0bd3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bd3-120">-DefaultProfile</span></span>
<span data-ttu-id="a0bd3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0bd3-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="a0bd3-122">-DomainFqdn</span></span>
<span data-ttu-id="a0bd3-123">Etki alanının tam nitelikli adı</span><span class="sxs-lookup"><span data-stu-id="a0bd3-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="a0bd3-124">-Filesharewnesspath</span><span class="sxs-lookup"><span data-stu-id="a0bd3-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="a0bd3-125">FileShare tanığı için isteğe bağlı yol</span><span class="sxs-lookup"><span data-stu-id="a0bd3-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="a0bd3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0bd3-126">-InputObject</span></span>
<span data-ttu-id="a0bd3-127">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="a0bd3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0bd3-128">-Name</span></span>
<span data-ttu-id="a0bd3-129">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a0bd3-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="a0bd3-130">-OuPath</span></span>
<span data-ttu-id="a0bd3-131">Düğümlerin ve kümenin sunulabilecek kuruluş birimi yolu</span><span class="sxs-lookup"><span data-stu-id="a0bd3-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="a0bd3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bd3-132">-ResourceGroupName</span></span>
<span data-ttu-id="a0bd3-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0bd3-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0bd3-134">-ResourceId</span></span>
<span data-ttu-id="a0bd3-135">SQL sanal makine grubu kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="a0bd3-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="a0bd3-136">-SqlServiceAccount</span></span>
<span data-ttu-id="a0bd3-137">SQL hizmetinin kümedeki tüm katılan SQL sanal makinelerinde çalışacağı ad</span><span class="sxs-lookup"><span data-stu-id="a0bd3-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="a0bd3-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a0bd3-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="a0bd3-139">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="a0bd3-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bd3-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="a0bd3-140">-StorageAccountUrl</span></span>
<span data-ttu-id="a0bd3-141">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="a0bd3-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="a0bd3-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a0bd3-142">-Tag</span></span>
<span data-ttu-id="a0bd3-143">SQL sanal makine grubuyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bd3-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0bd3-144">-Confirm</span></span>
<span data-ttu-id="a0bd3-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bd3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bd3-146">-WhatIf</span></span>
<span data-ttu-id="a0bd3-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bd3-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bd3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bd3-149">CommonParameters</span></span>
<span data-ttu-id="a0bd3-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bd3-151">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0bd3-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bd3-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0bd3-152">INPUTS</span></span>

### <span data-ttu-id="a0bd3-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="a0bd3-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="a0bd3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a0bd3-154">System.String</span></span>

## <span data-ttu-id="a0bd3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0bd3-155">OUTPUTS</span></span>

### <span data-ttu-id="a0bd3-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="a0bd3-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a0bd3-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0bd3-157">NOTES</span></span>

## <span data-ttu-id="a0bd3-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0bd3-158">RELATED LINKS</span></span>
