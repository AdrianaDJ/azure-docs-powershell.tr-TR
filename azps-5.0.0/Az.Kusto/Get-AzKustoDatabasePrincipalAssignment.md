---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279009"
---
# <span data-ttu-id="97596-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="97596-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="97596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97596-102">SYNOPSIS</span></span>
<span data-ttu-id="97596-103">Kusto küme veritabanı principalAssignment alır.</span><span class="sxs-lookup"><span data-stu-id="97596-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="97596-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97596-104">SYNTAX</span></span>

### <span data-ttu-id="97596-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97596-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97596-106">Al</span><span class="sxs-lookup"><span data-stu-id="97596-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97596-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="97596-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="97596-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97596-108">DESCRIPTION</span></span>
<span data-ttu-id="97596-109">Kusto küme veritabanı principalAssignment alır.</span><span class="sxs-lookup"><span data-stu-id="97596-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="97596-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97596-110">EXAMPLES</span></span>

### <span data-ttu-id="97596-111">Örnek 1: veritabanındaki tüm PrincipalAssignment ada göre listeler</span><span class="sxs-lookup"><span data-stu-id="97596-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="97596-112">Yukarıdaki komut, "testnewkustocluster" kümesinde bulunan "mykustodatabase" veritabanındaki tüm PrincipalAssignment 'i döndürür.</span><span class="sxs-lookup"><span data-stu-id="97596-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="97596-113">Örnek 2: adla veritabanında belirli bir PrincipalAssignment alma</span><span class="sxs-lookup"><span data-stu-id="97596-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="97596-114">Yukarıdaki komut, "testnewkustocluster" kümesinde bulunan "mykustodatabase" veritabanındaki tüm tüm PrincipalAssignment "kustoprincipal1" döndürür.</span><span class="sxs-lookup"><span data-stu-id="97596-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="97596-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97596-115">PARAMETERS</span></span>

### <span data-ttu-id="97596-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="97596-116">-ClusterName</span></span>
<span data-ttu-id="97596-117">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="97596-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97596-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97596-118">-DatabaseName</span></span>
<span data-ttu-id="97596-119">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="97596-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97596-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97596-120">-DefaultProfile</span></span>
<span data-ttu-id="97596-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97596-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97596-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97596-122">-InputObject</span></span>
<span data-ttu-id="97596-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97596-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97596-124">-Princıpalassignmentname</span><span class="sxs-lookup"><span data-stu-id="97596-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="97596-125">Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="97596-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97596-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97596-126">-ResourceGroupName</span></span>
<span data-ttu-id="97596-127">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="97596-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97596-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="97596-128">-SubscriptionId</span></span>
<span data-ttu-id="97596-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="97596-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97596-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97596-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97596-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97596-131">CommonParameters</span></span>
<span data-ttu-id="97596-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97596-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97596-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97596-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97596-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97596-134">INPUTS</span></span>

### <span data-ttu-id="97596-135">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="97596-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="97596-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97596-136">OUTPUTS</span></span>

### <span data-ttu-id="97596-137">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="97596-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="97596-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97596-138">NOTES</span></span>

<span data-ttu-id="97596-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="97596-139">ALIASES</span></span>

<span data-ttu-id="97596-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="97596-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97596-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="97596-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97596-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97596-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97596-143">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="97596-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97596-144">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="97596-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="97596-145">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="97596-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="97596-146">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="97596-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="97596-147">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="97596-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="97596-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="97596-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97596-149">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="97596-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="97596-150">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="97596-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="97596-151">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="97596-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="97596-152">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="97596-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="97596-153">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97596-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="97596-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97596-154">RELATED LINKS</span></span>

