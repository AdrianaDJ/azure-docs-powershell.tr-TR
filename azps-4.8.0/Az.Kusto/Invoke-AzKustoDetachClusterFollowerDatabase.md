---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267330"
---
# <span data-ttu-id="19a9f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="19a9f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="19a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="19a9f-103">Bu kümenin sahip olduğu veritabanının tüm izleyicileri ayırır.</span><span class="sxs-lookup"><span data-stu-id="19a9f-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="19a9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19a9f-104">SYNTAX</span></span>

### <span data-ttu-id="19a9f-105">Çıkarılabilir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19a9f-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19a9f-106">Çıkarılabilir Viaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="19a9f-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19a9f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="19a9f-107">DESCRIPTION</span></span>
<span data-ttu-id="19a9f-108">Bu kümenin sahip olduğu veritabanının tüm izleyicileri ayırır.</span><span class="sxs-lookup"><span data-stu-id="19a9f-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="19a9f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19a9f-109">EXAMPLES</span></span>

### <span data-ttu-id="19a9f-110">Örnek 1: bir izleyici veritabanını ayırma</span><span class="sxs-lookup"><span data-stu-id="19a9f-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="19a9f-111">Yukarıdaki komut, AttachedDatabaseConfiguration "myizleme", "testnewkustoclusterf" kümesinden tanımlanan izleme veritabanını ayırır.</span><span class="sxs-lookup"><span data-stu-id="19a9f-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="19a9f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19a9f-112">PARAMETERS</span></span>

### <span data-ttu-id="19a9f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="19a9f-113">-AsJob</span></span>
<span data-ttu-id="19a9f-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="19a9f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="19a9f-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="19a9f-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="19a9f-116">İzleyici kümesindeki eklenmiş veritabanı yapılandırmasının kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="19a9f-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="19a9f-117">-ClusterName</span></span>
<span data-ttu-id="19a9f-118">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19a9f-119">-Clusterresourceıd</span><span class="sxs-lookup"><span data-stu-id="19a9f-119">-ClusterResourceId</span></span>
<span data-ttu-id="19a9f-120">Bu kümenin sahip olduğu bir veritabanını izleyen kümenin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="19a9f-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="19a9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a9f-121">-DefaultProfile</span></span>
<span data-ttu-id="19a9f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19a9f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19a9f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19a9f-123">-InputObject</span></span>
<span data-ttu-id="19a9f-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19a9f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19a9f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19a9f-125">-NoWait</span></span>
<span data-ttu-id="19a9f-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="19a9f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19a9f-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="19a9f-127">-PassThru</span></span>
<span data-ttu-id="19a9f-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="19a9f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19a9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="19a9f-130">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19a9f-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="19a9f-131">-SubscriptionId</span></span>
<span data-ttu-id="19a9f-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="19a9f-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="19a9f-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19a9f-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19a9f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="19a9f-134">-Confirm</span></span>
<span data-ttu-id="19a9f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19a9f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19a9f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19a9f-136">-WhatIf</span></span>
<span data-ttu-id="19a9f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19a9f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19a9f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19a9f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19a9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a9f-139">CommonParameters</span></span>
<span data-ttu-id="19a9f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19a9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a9f-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19a9f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a9f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19a9f-142">INPUTS</span></span>

### <span data-ttu-id="19a9f-143">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="19a9f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="19a9f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19a9f-144">OUTPUTS</span></span>

### <span data-ttu-id="19a9f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19a9f-145">System.Boolean</span></span>

## <span data-ttu-id="19a9f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19a9f-146">NOTES</span></span>

<span data-ttu-id="19a9f-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="19a9f-147">ALIASES</span></span>

<span data-ttu-id="19a9f-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="19a9f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19a9f-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="19a9f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19a9f-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19a9f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19a9f-151">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="19a9f-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19a9f-152">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="19a9f-153">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="19a9f-154">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="19a9f-155">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="19a9f-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="19a9f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19a9f-157">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="19a9f-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="19a9f-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="19a9f-159">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="19a9f-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="19a9f-160">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="19a9f-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="19a9f-161">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19a9f-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="19a9f-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19a9f-162">RELATED LINKS</span></span>

