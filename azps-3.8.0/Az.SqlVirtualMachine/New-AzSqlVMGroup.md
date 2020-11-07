---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937924"
---
# <span data-ttu-id="66953-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="66953-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="66953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66953-102">SYNOPSIS</span></span>
<span data-ttu-id="66953-103">Yeni bir SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66953-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="66953-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66953-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66953-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66953-105">DESCRIPTION</span></span>
<span data-ttu-id="66953-106">New-AzSqlVMGroup cmdlet 'i bir Azure SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66953-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="66953-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66953-107">EXAMPLES</span></span>

### <span data-ttu-id="66953-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66953-108">Example 1</span></span>
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

<span data-ttu-id="66953-109">ResourceGroup01 kaynak grubunda test-Group VM ile yeni bir Azure SQL sanal makine grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66953-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="66953-110">$profile, Microsoft. Azure. Management. SqlVirtualMachine. modeller. WsfcDomainProfile türünde bir nesnedir</span><span class="sxs-lookup"><span data-stu-id="66953-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="66953-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66953-111">PARAMETERS</span></span>

### <span data-ttu-id="66953-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="66953-112">-AsJob</span></span>
<span data-ttu-id="66953-113">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="66953-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="66953-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="66953-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="66953-115">Küme oluştururken kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="66953-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="66953-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="66953-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="66953-117">İşletim kümesi için kullanılan ad</span><span class="sxs-lookup"><span data-stu-id="66953-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="66953-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66953-118">-DefaultProfile</span></span>
<span data-ttu-id="66953-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66953-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66953-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="66953-120">-DomainFqdn</span></span>
<span data-ttu-id="66953-121">Etki alanının tam nitelikli adı</span><span class="sxs-lookup"><span data-stu-id="66953-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="66953-122">-Filesharewnesspath</span><span class="sxs-lookup"><span data-stu-id="66953-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="66953-123">FileShare tanığı için isteğe bağlı yol</span><span class="sxs-lookup"><span data-stu-id="66953-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="66953-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="66953-124">-Location</span></span>
<span data-ttu-id="66953-125">SQL sanal makine grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="66953-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="66953-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="66953-126">-Name</span></span>
<span data-ttu-id="66953-127">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="66953-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="66953-128">-Teklif</span><span class="sxs-lookup"><span data-stu-id="66953-128">-Offer</span></span>
<span data-ttu-id="66953-129">SQL sanal makine grubu teklifi.</span><span class="sxs-lookup"><span data-stu-id="66953-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="66953-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="66953-130">-OuPath</span></span>
<span data-ttu-id="66953-131">Düğümlerin ve kümenin sunulabilecek kuruluş birimi yolu</span><span class="sxs-lookup"><span data-stu-id="66953-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="66953-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66953-132">-ResourceGroupName</span></span>
<span data-ttu-id="66953-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66953-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="66953-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="66953-134">-Sku</span></span>
<span data-ttu-id="66953-135">SQL sanal makine grubu sürüm türü.</span><span class="sxs-lookup"><span data-stu-id="66953-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="66953-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="66953-136">-SqlServiceAccount</span></span>
<span data-ttu-id="66953-137">SQL hizmetinin kümedeki tüm katılan SQL sanal makinelerinde çalışacağı ad</span><span class="sxs-lookup"><span data-stu-id="66953-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="66953-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="66953-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="66953-139">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="66953-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="66953-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="66953-140">-StorageAccountUrl</span></span>
<span data-ttu-id="66953-141">Tanık depolama hesabının birincil anahtarı</span><span class="sxs-lookup"><span data-stu-id="66953-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="66953-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="66953-142">-Tag</span></span>
<span data-ttu-id="66953-143">SQL sanal makine grubuyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="66953-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="66953-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="66953-144">-Confirm</span></span>
<span data-ttu-id="66953-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66953-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66953-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66953-146">-WhatIf</span></span>
<span data-ttu-id="66953-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66953-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66953-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66953-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66953-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66953-149">CommonParameters</span></span>
<span data-ttu-id="66953-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66953-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66953-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66953-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66953-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66953-152">INPUTS</span></span>

### <span data-ttu-id="66953-153">System. String</span><span class="sxs-lookup"><span data-stu-id="66953-153">System.String</span></span>

## <span data-ttu-id="66953-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66953-154">OUTPUTS</span></span>

### <span data-ttu-id="66953-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="66953-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="66953-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66953-156">NOTES</span></span>

## <span data-ttu-id="66953-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66953-157">RELATED LINKS</span></span>
