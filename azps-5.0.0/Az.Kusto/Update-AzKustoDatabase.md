---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277715"
---
# <span data-ttu-id="0cd80-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="0cd80-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="0cd80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd80-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd80-103">Bir veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-103">Updates a database.</span></span>

## <span data-ttu-id="0cd80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cd80-104">SYNTAX</span></span>

### <span data-ttu-id="0cd80-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0cd80-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0cd80-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="0cd80-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0cd80-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cd80-107">DESCRIPTION</span></span>
<span data-ttu-id="0cd80-108">Bir veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-108">Updates a database.</span></span>

## <span data-ttu-id="0cd80-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cd80-109">EXAMPLES</span></span>

### <span data-ttu-id="0cd80-110">Örnek 1: var olan veritabanını adla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0cd80-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="0cd80-111">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "testnewkustocluster" kümesinde "mykustodatabase" kusto veritabanının yumuşak silme süresini ve etkin önbellek süresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="0cd80-112">Örnek 2: kimlik aracılığıyla varolan veritabanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0cd80-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="0cd80-113">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "testnewkustocluster" kümesinde "mykustodatabase" kusto veritabanının yumuşak silme süresini ve etkin önbellek süresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="0cd80-114">Örnek 3: var olan ReadOnly veritabanını adla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0cd80-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="0cd80-115">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "mykustodatabase" kümesindeki "" kusto veritabanının etkin önbellek dönemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="0cd80-116">Örnek 4: kimlik aracılığıyla var olan salt okunur veritabanını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0cd80-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="0cd80-117">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "mykustodatabase" kümesindeki "" kusto veritabanının etkin önbellek dönemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="0cd80-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cd80-118">PARAMETERS</span></span>

### <span data-ttu-id="0cd80-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="0cd80-119">-AsJob</span></span>
<span data-ttu-id="0cd80-120">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="0cd80-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0cd80-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0cd80-121">-ClusterName</span></span>
<span data-ttu-id="0cd80-122">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd80-123">-DefaultProfile</span></span>
<span data-ttu-id="0cd80-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0cd80-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-125">-Hotcachedönem</span><span class="sxs-lookup"><span data-stu-id="0cd80-125">-HotCachePeriod</span></span>
<span data-ttu-id="0cd80-126">Verilerin TimeSpan 'teki hızlı sorgular için önbellekte tutulması gereken süre.</span><span class="sxs-lookup"><span data-stu-id="0cd80-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cd80-127">-InputObject</span></span>
<span data-ttu-id="0cd80-128">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0cd80-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="0cd80-129">-Kind</span></span>
<span data-ttu-id="0cd80-130">Veritabanı türü</span><span class="sxs-lookup"><span data-stu-id="0cd80-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="0cd80-131">-Location</span></span>
<span data-ttu-id="0cd80-132">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="0cd80-132">Resource location.</span></span>

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

### <span data-ttu-id="0cd80-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cd80-133">-Name</span></span>
<span data-ttu-id="0cd80-134">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0cd80-135">-NoWait</span></span>
<span data-ttu-id="0cd80-136">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="0cd80-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0cd80-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd80-137">-ResourceGroupName</span></span>
<span data-ttu-id="0cd80-138">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-139">-Softdeletedönem</span><span class="sxs-lookup"><span data-stu-id="0cd80-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="0cd80-140">Verilerin TimeSpan 'teki sorguların erişimini durdurmadan önce tutulacağı süre.</span><span class="sxs-lookup"><span data-stu-id="0cd80-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-141">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0cd80-141">-SubscriptionId</span></span>
<span data-ttu-id="0cd80-142">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0cd80-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0cd80-143">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0cd80-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd80-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="0cd80-144">-Confirm</span></span>
<span data-ttu-id="0cd80-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0cd80-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd80-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd80-146">-WhatIf</span></span>
<span data-ttu-id="0cd80-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cd80-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd80-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0cd80-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd80-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd80-149">CommonParameters</span></span>
<span data-ttu-id="0cd80-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cd80-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd80-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0cd80-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd80-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cd80-152">INPUTS</span></span>

### <span data-ttu-id="0cd80-153">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="0cd80-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0cd80-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cd80-154">OUTPUTS</span></span>

### <span data-ttu-id="0cd80-155">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="0cd80-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="0cd80-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cd80-156">NOTES</span></span>

<span data-ttu-id="0cd80-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0cd80-157">ALIASES</span></span>

<span data-ttu-id="0cd80-158">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0cd80-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0cd80-159">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0cd80-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0cd80-160">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0cd80-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0cd80-161">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0cd80-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0cd80-162">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0cd80-163">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0cd80-164">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0cd80-165">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0cd80-166">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0cd80-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0cd80-167">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="0cd80-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0cd80-168">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0cd80-169">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0cd80-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0cd80-170">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0cd80-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0cd80-171">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0cd80-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0cd80-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cd80-172">RELATED LINKS</span></span>

