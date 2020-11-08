---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109968"
---
# <span data-ttu-id="c9a3a-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c9a3a-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="c9a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a3a-103">Kusto kümesini alır principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c9a3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9a3a-104">SYNTAX</span></span>

### <span data-ttu-id="c9a3a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9a3a-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3a-106">Al</span><span class="sxs-lookup"><span data-stu-id="c9a3a-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c9a3a-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9a3a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9a3a-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a3a-109">Kusto kümesini alır principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="c9a3a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9a3a-110">EXAMPLES</span></span>

### <span data-ttu-id="c9a3a-111">Örnek 1: tüm kusto küme principalAssignment</span><span class="sxs-lookup"><span data-stu-id="c9a3a-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="c9a3a-112">Yukarıdaki komut "testnewkustocluster" kümesindeki tüm principalAssignment listeler.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c9a3a-113">Örnek 2: ada göre principalAssignment bir kusto kümesi alır</span><span class="sxs-lookup"><span data-stu-id="c9a3a-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="c9a3a-114">Yukarıdaki komut, "testnewkustocluster" kümesinde "kustoprincipal1" adlı kusto Cluster principalAssignment 'i döndürür.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c9a3a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9a3a-115">PARAMETERS</span></span>

### <span data-ttu-id="c9a3a-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c9a3a-116">-ClusterName</span></span>
<span data-ttu-id="c9a3a-117">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9a3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a3a-118">-DefaultProfile</span></span>
<span data-ttu-id="c9a3a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a3a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9a3a-120">-InputObject</span></span>
<span data-ttu-id="c9a3a-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9a3a-122">-Princıpalassignmentname</span><span class="sxs-lookup"><span data-stu-id="c9a3a-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="c9a3a-123">Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="c9a3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9a3a-125">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c9a3a-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c9a3a-126">-SubscriptionId</span></span>
<span data-ttu-id="c9a3a-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9a3a-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9a3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a3a-129">CommonParameters</span></span>
<span data-ttu-id="c9a3a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a3a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a3a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9a3a-132">INPUTS</span></span>

### <span data-ttu-id="c9a3a-133">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="c9a3a-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c9a3a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9a3a-134">OUTPUTS</span></span>

### <span data-ttu-id="c9a3a-135">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="c9a3a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="c9a3a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9a3a-136">NOTES</span></span>

<span data-ttu-id="c9a3a-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c9a3a-137">ALIASES</span></span>

<span data-ttu-id="c9a3a-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c9a3a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9a3a-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9a3a-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9a3a-141">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c9a3a-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9a3a-142">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c9a3a-143">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a3a-144">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c9a3a-145">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a3a-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c9a3a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9a3a-147">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c9a3a-148">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c9a3a-149">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c9a3a-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c9a3a-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c9a3a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c9a3a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9a3a-152">RELATED LINKS</span></span>

