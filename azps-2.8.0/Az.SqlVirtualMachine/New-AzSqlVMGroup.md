---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: e46df689b4cc6953f29f5361c4df8bc5bd878acd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933967"
---
# <span data-ttu-id="ab7ee-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ab7ee-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="ab7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7ee-103">Yeni bir SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="ab7ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab7ee-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab7ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab7ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ab7ee-106">New-AzSqlVMGroup cmdlet 'i bir Azure SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="ab7ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab7ee-107">EXAMPLES</span></span>

### <span data-ttu-id="ab7ee-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ab7ee-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ab7ee-109">ResourceGroup01 kaynak grubunda test-Group VM ile yeni bir Azure SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="ab7ee-110">$profile, Microsoft. Azure. Management. SqlVirtualMachine. modeller. WsfcDomainProfile türünde bir nesnedir</span><span class="sxs-lookup"><span data-stu-id="ab7ee-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="ab7ee-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab7ee-111">PARAMETERS</span></span>

### <span data-ttu-id="ab7ee-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="ab7ee-112">-AsJob</span></span>
<span data-ttu-id="ab7ee-113">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ab7ee-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="ab7ee-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="ab7ee-115">Küme oluştururken kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="ab7ee-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="ab7ee-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="ab7ee-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="ab7ee-117">İşletim kümesi için kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="ab7ee-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="ab7ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7ee-118">-DefaultProfile</span></span>
<span data-ttu-id="ab7ee-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab7ee-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="ab7ee-120">-DomainFqdn</span></span>
<span data-ttu-id="ab7ee-121">Etki alanının tam nitelikli adı</span><span class="sxs-lookup"><span data-stu-id="ab7ee-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="ab7ee-122">-Filesharewnesspath</span><span class="sxs-lookup"><span data-stu-id="ab7ee-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="ab7ee-123">FileShare tanığı için isteğe bağlı yol</span><span class="sxs-lookup"><span data-stu-id="ab7ee-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="ab7ee-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="ab7ee-124">-Location</span></span>
<span data-ttu-id="ab7ee-125">SQL sanal makine grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="ab7ee-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab7ee-126">-Name</span></span>
<span data-ttu-id="ab7ee-127">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7ee-128">-Teklif</span><span class="sxs-lookup"><span data-stu-id="ab7ee-128">-Offer</span></span>
<span data-ttu-id="ab7ee-129">SQL sanal makine grubu teklifi.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="ab7ee-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="ab7ee-130">-OuPath</span></span>
<span data-ttu-id="ab7ee-131">Düğümlerin ve kümenin sunulabilecek kuruluş birimi yolu</span><span class="sxs-lookup"><span data-stu-id="ab7ee-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="ab7ee-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7ee-132">-ResourceGroupName</span></span>
<span data-ttu-id="ab7ee-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7ee-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="ab7ee-134">-Sku</span></span>
<span data-ttu-id="ab7ee-135">SQL sanal makine grubu sürüm türü.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="ab7ee-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ab7ee-136">-SqlServiceAccount</span></span>
<span data-ttu-id="ab7ee-137">SQL hizmetinin kümedeki tüm katılan SQL sanal makinelerinde çalışacağı ad</span><span class="sxs-lookup"><span data-stu-id="ab7ee-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="ab7ee-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ab7ee-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="ab7ee-139">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="ab7ee-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7ee-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ab7ee-140">-StorageAccountUrl</span></span>
<span data-ttu-id="ab7ee-141">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="ab7ee-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="ab7ee-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ab7ee-142">-Tag</span></span>
<span data-ttu-id="ab7ee-143">SQL sanal makine grubuyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="ab7ee-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab7ee-144">-Confirm</span></span>
<span data-ttu-id="ab7ee-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab7ee-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab7ee-146">-WhatIf</span></span>
<span data-ttu-id="ab7ee-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab7ee-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab7ee-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7ee-149">CommonParameters</span></span>
<span data-ttu-id="ab7ee-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7ee-151">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ab7ee-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7ee-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab7ee-152">INPUTS</span></span>

### <span data-ttu-id="ab7ee-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ab7ee-153">System.String</span></span>

## <span data-ttu-id="ab7ee-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab7ee-154">OUTPUTS</span></span>

### <span data-ttu-id="ab7ee-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="ab7ee-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ab7ee-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab7ee-156">NOTES</span></span>

## <span data-ttu-id="ab7ee-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab7ee-157">RELATED LINKS</span></span>
