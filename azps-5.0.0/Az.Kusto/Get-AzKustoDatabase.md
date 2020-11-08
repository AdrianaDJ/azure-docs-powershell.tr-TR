---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279013"
---
# <span data-ttu-id="68da3-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="68da3-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="68da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68da3-102">SYNOPSIS</span></span>
<span data-ttu-id="68da3-103">Bir veritabanı döndürür.</span><span class="sxs-lookup"><span data-stu-id="68da3-103">Returns a database.</span></span>

## <span data-ttu-id="68da3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68da3-104">SYNTAX</span></span>

### <span data-ttu-id="68da3-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68da3-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="68da3-106">Al</span><span class="sxs-lookup"><span data-stu-id="68da3-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="68da3-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="68da3-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="68da3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="68da3-108">DESCRIPTION</span></span>
<span data-ttu-id="68da3-109">Bir veritabanı döndürür.</span><span class="sxs-lookup"><span data-stu-id="68da3-109">Returns a database.</span></span>

## <span data-ttu-id="68da3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68da3-110">EXAMPLES</span></span>

### <span data-ttu-id="68da3-111">Örnek 1: kümedeki tüm kusto veritabanlarını ada göre listeler</span><span class="sxs-lookup"><span data-stu-id="68da3-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="68da3-112">Yukarıdaki komut, "testnewkustocluster" kaynak grubunda bulunan "" kümesindeki tüm kusto veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="68da3-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="68da3-113">Örnek 2: adla belirli bir kusto veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="68da3-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="68da3-114">Yukarıdaki komut, "mykustodatabase" adlı kusto veritabanını, "testrg" kaynak grubunda bulunan "testnewkustocluster" kümesinde döndürür.</span><span class="sxs-lookup"><span data-stu-id="68da3-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="68da3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68da3-115">PARAMETERS</span></span>

### <span data-ttu-id="68da3-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="68da3-116">-ClusterName</span></span>
<span data-ttu-id="68da3-117">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="68da3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68da3-118">-DefaultProfile</span></span>
<span data-ttu-id="68da3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68da3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68da3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68da3-120">-InputObject</span></span>
<span data-ttu-id="68da3-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68da3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68da3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="68da3-122">-Name</span></span>
<span data-ttu-id="68da3-123">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68da3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68da3-124">-ResourceGroupName</span></span>
<span data-ttu-id="68da3-125">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="68da3-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="68da3-126">-SubscriptionId</span></span>
<span data-ttu-id="68da3-127">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="68da3-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="68da3-128">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68da3-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="68da3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68da3-129">CommonParameters</span></span>
<span data-ttu-id="68da3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68da3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68da3-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68da3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68da3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68da3-132">INPUTS</span></span>

### <span data-ttu-id="68da3-133">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="68da3-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="68da3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68da3-134">OUTPUTS</span></span>

### <span data-ttu-id="68da3-135">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="68da3-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="68da3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68da3-136">NOTES</span></span>

<span data-ttu-id="68da3-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="68da3-137">ALIASES</span></span>

<span data-ttu-id="68da3-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="68da3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68da3-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="68da3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68da3-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68da3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68da3-141">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="68da3-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68da3-142">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="68da3-143">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="68da3-144">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="68da3-145">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="68da3-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="68da3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68da3-147">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="68da3-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="68da3-148">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="68da3-149">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="68da3-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="68da3-150">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="68da3-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="68da3-151">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68da3-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="68da3-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68da3-152">RELATED LINKS</span></span>

