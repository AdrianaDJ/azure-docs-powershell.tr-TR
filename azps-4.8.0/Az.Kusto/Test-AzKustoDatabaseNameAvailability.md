---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109580"
---
# <span data-ttu-id="ecb4a-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ecb4a-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="ecb4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb4a-103">Veritabanı adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="ecb4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecb4a-104">SYNTAX</span></span>

### <span data-ttu-id="ecb4a-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ecb4a-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb4a-106">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="ecb4a-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecb4a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecb4a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb4a-108">Veritabanı adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="ecb4a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecb4a-109">EXAMPLES</span></span>

### <span data-ttu-id="ecb4a-110">Örnek 1: kullanımda olan bir kusto veritabanı adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="ecb4a-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="ecb4a-111">Yukarıdaki komut, "mykustodatabase" adlı kusto veritabanının "testnewkustocluster" kümesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="ecb4a-112">Örnek 2: kullanımda olmayan bir kusto veritabanı adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="ecb4a-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="ecb4a-113">Yukarıdaki komut, "mykustodatabase2" adlı kusto veritabanının "testnewkustocluster" kümesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="ecb4a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecb4a-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb4a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ecb4a-115">-ClusterName</span></span>
<span data-ttu-id="ecb4a-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ecb4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb4a-117">-DefaultProfile</span></span>
<span data-ttu-id="ecb4a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb4a-119">-InputObject</span></span>
<span data-ttu-id="ecb4a-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ecb4a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ecb4a-121">-Name</span></span>
<span data-ttu-id="ecb4a-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-122">Resource name.</span></span>

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

### <span data-ttu-id="ecb4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ecb4a-124">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ecb4a-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ecb4a-125">-SubscriptionId</span></span>
<span data-ttu-id="ecb4a-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ecb4a-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ecb4a-128">-Tür</span><span class="sxs-lookup"><span data-stu-id="ecb4a-128">-Type</span></span>
<span data-ttu-id="ecb4a-129">Microsoft. kusto/kümeler/veritabanları için kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="ecb4a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ecb4a-130">-Confirm</span></span>
<span data-ttu-id="ecb4a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb4a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb4a-132">-WhatIf</span></span>
<span data-ttu-id="ecb4a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb4a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb4a-135">CommonParameters</span></span>
<span data-ttu-id="ecb4a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb4a-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb4a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecb4a-138">INPUTS</span></span>

### <span data-ttu-id="ecb4a-139">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="ecb4a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ecb4a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecb4a-140">OUTPUTS</span></span>

### <span data-ttu-id="ecb4a-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ecb4a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ecb4a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecb4a-142">NOTES</span></span>

<span data-ttu-id="ecb4a-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ecb4a-143">ALIASES</span></span>

<span data-ttu-id="ecb4a-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ecb4a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ecb4a-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecb4a-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ecb4a-147">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ecb4a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ecb4a-148">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ecb4a-149">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ecb4a-150">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ecb4a-151">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ecb4a-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ecb4a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ecb4a-153">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ecb4a-154">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ecb4a-155">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ecb4a-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ecb4a-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ecb4a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecb4a-158">RELATED LINKS</span></span>

