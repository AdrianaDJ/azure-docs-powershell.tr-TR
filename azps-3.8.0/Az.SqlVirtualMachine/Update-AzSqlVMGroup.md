---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096550"
---
# <span data-ttu-id="53a3b-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="53a3b-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="53a3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="53a3b-103">SQL sanal makine grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="53a3b-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="53a3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53a3b-104">SYNTAX</span></span>

### <span data-ttu-id="53a3b-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53a3b-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53a3b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="53a3b-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a3b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="53a3b-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a3b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="53a3b-108">DESCRIPTION</span></span>
<span data-ttu-id="53a3b-109">Update-AzSqlVMGroup cmdlet 'i bir SQL sanal makine grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="53a3b-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="53a3b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53a3b-110">EXAMPLES</span></span>

### <span data-ttu-id="53a3b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53a3b-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="53a3b-112">SQL sanal makine grubunun etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="53a3b-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="53a3b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53a3b-113">PARAMETERS</span></span>

### <span data-ttu-id="53a3b-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="53a3b-114">-AsJob</span></span>
<span data-ttu-id="53a3b-115">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="53a3b-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="53a3b-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="53a3b-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="53a3b-117">Küme oluştururken kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="53a3b-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="53a3b-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="53a3b-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="53a3b-119">İşletim kümesi için kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="53a3b-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="53a3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a3b-120">-DefaultProfile</span></span>
<span data-ttu-id="53a3b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53a3b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a3b-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="53a3b-122">-DomainFqdn</span></span>
<span data-ttu-id="53a3b-123">Etki alanının tam nitelikli adı</span><span class="sxs-lookup"><span data-stu-id="53a3b-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="53a3b-124">-Filesharewnesspath</span><span class="sxs-lookup"><span data-stu-id="53a3b-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="53a3b-125">FileShare tanığı için isteğe bağlı yol</span><span class="sxs-lookup"><span data-stu-id="53a3b-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="53a3b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a3b-126">-InputObject</span></span>
<span data-ttu-id="53a3b-127">SQL sanal makinesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="53a3b-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="53a3b-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="53a3b-128">-Name</span></span>
<span data-ttu-id="53a3b-129">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="53a3b-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="53a3b-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="53a3b-130">-OuPath</span></span>
<span data-ttu-id="53a3b-131">Düğümlerin ve kümenin sunulabilecek kuruluş birimi yolu</span><span class="sxs-lookup"><span data-stu-id="53a3b-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="53a3b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a3b-132">-ResourceGroupName</span></span>
<span data-ttu-id="53a3b-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="53a3b-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="53a3b-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53a3b-134">-ResourceId</span></span>
<span data-ttu-id="53a3b-135">SQL sanal makine grubu kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="53a3b-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="53a3b-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="53a3b-136">-SqlServiceAccount</span></span>
<span data-ttu-id="53a3b-137">SQL hizmetinin kümedeki tüm katılan SQL sanal makinelerinde çalışacağı ad</span><span class="sxs-lookup"><span data-stu-id="53a3b-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="53a3b-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="53a3b-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="53a3b-139">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="53a3b-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="53a3b-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="53a3b-140">-StorageAccountUrl</span></span>
<span data-ttu-id="53a3b-141">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="53a3b-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="53a3b-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="53a3b-142">-Tag</span></span>
<span data-ttu-id="53a3b-143">SQL sanal makine grubuyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="53a3b-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="53a3b-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="53a3b-144">-Confirm</span></span>
<span data-ttu-id="53a3b-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="53a3b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a3b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a3b-146">-WhatIf</span></span>
<span data-ttu-id="53a3b-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53a3b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a3b-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="53a3b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a3b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a3b-149">CommonParameters</span></span>
<span data-ttu-id="53a3b-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53a3b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a3b-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="53a3b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a3b-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53a3b-152">INPUTS</span></span>

### <span data-ttu-id="53a3b-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="53a3b-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="53a3b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="53a3b-154">System.String</span></span>

## <span data-ttu-id="53a3b-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53a3b-155">OUTPUTS</span></span>

### <span data-ttu-id="53a3b-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="53a3b-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="53a3b-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53a3b-157">NOTES</span></span>

## <span data-ttu-id="53a3b-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53a3b-158">RELATED LINKS</span></span>
