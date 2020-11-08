---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267331"
---
# <span data-ttu-id="6b748-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6b748-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="6b748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b748-102">SYNOPSIS</span></span>
<span data-ttu-id="6b748-103">Veri bağlantısı adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="6b748-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="6b748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b748-104">SYNTAX</span></span>

### <span data-ttu-id="6b748-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b748-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b748-106">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="6b748-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b748-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b748-107">DESCRIPTION</span></span>
<span data-ttu-id="6b748-108">Veri bağlantısı adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="6b748-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="6b748-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b748-109">EXAMPLES</span></span>

### <span data-ttu-id="6b748-110">Örnek 1: kullanımda olan bir veri bağlantısı adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="6b748-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="6b748-111">Yukarıdaki komut, "mykustodatabase" veritabanında "mykustodataconnection" adlı bir veri bağlantısının bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="6b748-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="6b748-112">Örnek 2: kullanımda olmayan bir veri bağlantısı adının uygunluk durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="6b748-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="6b748-113">Yukarıdaki komut "mydataconnection" adlı bir veri bağlantısının "mykustodatabase" veritabanında bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="6b748-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="6b748-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b748-114">PARAMETERS</span></span>

### <span data-ttu-id="6b748-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6b748-115">-ClusterName</span></span>
<span data-ttu-id="6b748-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6b748-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b748-117">-DatabaseName</span></span>
<span data-ttu-id="6b748-118">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="6b748-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b748-119">-DefaultProfile</span></span>
<span data-ttu-id="6b748-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b748-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b748-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b748-121">-InputObject</span></span>
<span data-ttu-id="6b748-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b748-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b748-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b748-123">-Name</span></span>
<span data-ttu-id="6b748-124">Veri bağlantısı adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-124">Data Connection name.</span></span>

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

### <span data-ttu-id="6b748-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b748-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b748-126">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6b748-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6b748-127">-SubscriptionId</span></span>
<span data-ttu-id="6b748-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b748-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6b748-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b748-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6b748-130">-Tür</span><span class="sxs-lookup"><span data-stu-id="6b748-130">-Type</span></span>
<span data-ttu-id="6b748-131">Kaynak, Microsoft. kusto/kümeler/veritabanları/veri bağlantıları türü.</span><span class="sxs-lookup"><span data-stu-id="6b748-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="6b748-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b748-132">-Confirm</span></span>
<span data-ttu-id="6b748-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b748-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b748-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b748-134">-WhatIf</span></span>
<span data-ttu-id="6b748-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b748-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b748-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b748-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b748-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b748-137">CommonParameters</span></span>
<span data-ttu-id="6b748-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b748-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b748-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b748-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b748-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b748-140">INPUTS</span></span>

### <span data-ttu-id="6b748-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="6b748-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="6b748-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b748-142">OUTPUTS</span></span>

### <span data-ttu-id="6b748-143">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="6b748-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="6b748-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b748-144">NOTES</span></span>

<span data-ttu-id="6b748-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6b748-145">ALIASES</span></span>

<span data-ttu-id="6b748-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6b748-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b748-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b748-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b748-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b748-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b748-149">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6b748-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b748-150">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="6b748-151">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="6b748-152">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="6b748-153">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="6b748-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6b748-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b748-155">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="6b748-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="6b748-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="6b748-157">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b748-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="6b748-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6b748-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6b748-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b748-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6b748-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b748-160">RELATED LINKS</span></span>

