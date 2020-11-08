---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277720"
---
# <span data-ttu-id="18b53-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="18b53-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="18b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b53-102">SYNOPSIS</span></span>
<span data-ttu-id="18b53-103">Veritabanı asıl atamasının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="18b53-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="18b53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18b53-104">SYNTAX</span></span>

### <span data-ttu-id="18b53-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18b53-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18b53-106">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="18b53-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18b53-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="18b53-107">DESCRIPTION</span></span>
<span data-ttu-id="18b53-108">Veritabanı asıl atamasının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="18b53-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="18b53-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18b53-109">EXAMPLES</span></span>

### <span data-ttu-id="18b53-110">Örnek 1: kullanımda olan bir veritabanı principalassignment adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="18b53-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="18b53-111">Yukarıdaki komut, "myprincipal" adındaki bir PrincipalAssignment "testnewkustocluster" kümesinden "mykustodatabase" veritabanında bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="18b53-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="18b53-112">Örnek 2: kullanımda olmayan bir veritabanı principalassignment adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="18b53-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="18b53-113">Yukarıdaki komut, "myprincipal" adındaki bir PrincipalAssignment "testnewkustocluster" kümesinden "mykustodatabase" veritabanında bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="18b53-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="18b53-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18b53-114">PARAMETERS</span></span>

### <span data-ttu-id="18b53-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="18b53-115">-ClusterName</span></span>
<span data-ttu-id="18b53-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18b53-117">-DatabaseName</span></span>
<span data-ttu-id="18b53-118">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b53-119">-DefaultProfile</span></span>
<span data-ttu-id="18b53-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18b53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b53-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b53-121">-InputObject</span></span>
<span data-ttu-id="18b53-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18b53-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="18b53-123">-Name</span></span>
<span data-ttu-id="18b53-124">Sorumlu atama kaynağı adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="18b53-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b53-125">-ResourceGroupName</span></span>
<span data-ttu-id="18b53-126">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="18b53-127">-SubscriptionId</span></span>
<span data-ttu-id="18b53-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="18b53-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18b53-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="18b53-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-130">-Tür</span><span class="sxs-lookup"><span data-stu-id="18b53-130">-Type</span></span>
<span data-ttu-id="18b53-131">Kaynak türü, Microsoft. kusto/kümeler/veritabanları/Principalas,.</span><span class="sxs-lookup"><span data-stu-id="18b53-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b53-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="18b53-132">-Confirm</span></span>
<span data-ttu-id="18b53-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18b53-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b53-134">-WhatIf</span></span>
<span data-ttu-id="18b53-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18b53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b53-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18b53-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b53-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b53-137">CommonParameters</span></span>
<span data-ttu-id="18b53-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18b53-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b53-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18b53-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b53-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18b53-140">INPUTS</span></span>

### <span data-ttu-id="18b53-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="18b53-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="18b53-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18b53-142">OUTPUTS</span></span>

### <span data-ttu-id="18b53-143">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="18b53-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="18b53-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18b53-144">NOTES</span></span>

<span data-ttu-id="18b53-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="18b53-145">ALIASES</span></span>

<span data-ttu-id="18b53-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="18b53-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18b53-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="18b53-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18b53-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18b53-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18b53-149">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="18b53-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18b53-150">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="18b53-151">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="18b53-152">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="18b53-153">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="18b53-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="18b53-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18b53-155">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="18b53-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="18b53-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="18b53-157">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="18b53-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="18b53-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="18b53-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18b53-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="18b53-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18b53-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18b53-160">RELATED LINKS</span></span>

