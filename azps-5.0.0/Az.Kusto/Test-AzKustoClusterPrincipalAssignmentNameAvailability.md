---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280178"
---
# <span data-ttu-id="ea0e4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ea0e4-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="ea0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0e4-103">Asıl ödev adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ea0e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea0e4-104">SYNTAX</span></span>

### <span data-ttu-id="ea0e4-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea0e4-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ea0e4-106">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="ea0e4-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea0e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea0e4-107">DESCRIPTION</span></span>
<span data-ttu-id="ea0e4-108">Asıl ödev adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ea0e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea0e4-109">EXAMPLES</span></span>

### <span data-ttu-id="ea0e4-110">Örnek 1: kullanımda olan bir küme principalassignment adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="ea0e4-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="ea0e4-111">Yukarıdaki komut, "myprincipal" adındaki bir PrincipalAssignment "testnewkustocluster" kümesinde var olup olmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ea0e4-112">Örnek 2: kullanımda olmayan bir küme principalassignment adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="ea0e4-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ea0e4-113">Yukarıdaki komut "testnewkustocluster" kümesinde "NewPrincipal" adında bir PrincipalAssignment olup olmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ea0e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea0e4-114">PARAMETERS</span></span>

### <span data-ttu-id="ea0e4-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ea0e4-115">-ClusterName</span></span>
<span data-ttu-id="ea0e4-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ea0e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0e4-117">-DefaultProfile</span></span>
<span data-ttu-id="ea0e4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea0e4-119">-InputObject</span></span>
<span data-ttu-id="ea0e4-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea0e4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea0e4-121">-Name</span></span>
<span data-ttu-id="ea0e4-122">Sorumlu atama kaynağı adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="ea0e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea0e4-124">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ea0e4-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ea0e4-125">-SubscriptionId</span></span>
<span data-ttu-id="ea0e4-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea0e4-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ea0e4-128">-Tür</span><span class="sxs-lookup"><span data-stu-id="ea0e4-128">-Type</span></span>
<span data-ttu-id="ea0e4-129">Kaynak türü, Microsoft. kusto/kümeler/Princıpalas,.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="ea0e4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea0e4-130">-Confirm</span></span>
<span data-ttu-id="ea0e4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0e4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0e4-132">-WhatIf</span></span>
<span data-ttu-id="ea0e4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0e4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0e4-135">CommonParameters</span></span>
<span data-ttu-id="ea0e4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0e4-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0e4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea0e4-138">INPUTS</span></span>

### <span data-ttu-id="ea0e4-139">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="ea0e4-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ea0e4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea0e4-140">OUTPUTS</span></span>

### <span data-ttu-id="ea0e4-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ea0e4-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ea0e4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea0e4-142">NOTES</span></span>

<span data-ttu-id="ea0e4-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ea0e4-143">ALIASES</span></span>

<span data-ttu-id="ea0e4-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ea0e4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea0e4-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea0e4-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea0e4-147">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ea0e4-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea0e4-148">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ea0e4-149">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ea0e4-150">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ea0e4-151">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ea0e4-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ea0e4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea0e4-153">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ea0e4-154">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ea0e4-155">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ea0e4-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ea0e4-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ea0e4-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ea0e4-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea0e4-158">RELATED LINKS</span></span>

