---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279014"
---
# <span data-ttu-id="e3490-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="e3490-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="e3490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3490-102">SYNOPSIS</span></span>
<span data-ttu-id="e3490-103">Veri bağlantısı döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3490-103">Returns a data connection.</span></span>

## <span data-ttu-id="e3490-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3490-104">SYNTAX</span></span>

### <span data-ttu-id="e3490-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3490-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3490-106">Al</span><span class="sxs-lookup"><span data-stu-id="e3490-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3490-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="e3490-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3490-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3490-108">DESCRIPTION</span></span>
<span data-ttu-id="e3490-109">Veri bağlantısı döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3490-109">Returns a data connection.</span></span>

## <span data-ttu-id="e3490-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3490-110">EXAMPLES</span></span>

### <span data-ttu-id="e3490-111">Örnek 1: belirli bir veritabanındaki tüm veri bağlantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="e3490-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="e3490-112">Yukarıdaki komut, "testnewkustocluster" kaynak grubunda bulunan "" kümesindeki tüm kusto veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3490-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="e3490-113">Örnek 2: adla belirli bir veri bağlantısı alma</span><span class="sxs-lookup"><span data-stu-id="e3490-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="e3490-114">Yukarıdaki komut, "mykustodatabase" veritabanındaki "" veritabanındaki "" adlı veri bağlantısını, "testrg" kaynak grubunda bulundu.</span><span class="sxs-lookup"><span data-stu-id="e3490-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="e3490-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3490-115">PARAMETERS</span></span>

### <span data-ttu-id="e3490-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e3490-116">-ClusterName</span></span>
<span data-ttu-id="e3490-117">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e3490-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3490-118">-DatabaseName</span></span>
<span data-ttu-id="e3490-119">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="e3490-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3490-120">-DefaultProfile</span></span>
<span data-ttu-id="e3490-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3490-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3490-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3490-122">-InputObject</span></span>
<span data-ttu-id="e3490-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3490-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3490-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3490-124">-Name</span></span>
<span data-ttu-id="e3490-125">Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3490-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3490-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3490-127">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e3490-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e3490-128">-SubscriptionId</span></span>
<span data-ttu-id="e3490-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e3490-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3490-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e3490-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3490-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3490-131">CommonParameters</span></span>
<span data-ttu-id="e3490-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3490-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3490-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3490-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3490-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3490-134">INPUTS</span></span>

### <span data-ttu-id="e3490-135">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="e3490-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e3490-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3490-136">OUTPUTS</span></span>

### <span data-ttu-id="e3490-137">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıdataconnection</span><span class="sxs-lookup"><span data-stu-id="e3490-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="e3490-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3490-138">NOTES</span></span>

<span data-ttu-id="e3490-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e3490-139">ALIASES</span></span>

<span data-ttu-id="e3490-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="e3490-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3490-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e3490-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3490-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3490-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3490-143">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="e3490-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3490-144">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e3490-145">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e3490-146">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e3490-147">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e3490-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e3490-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3490-149">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="e3490-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e3490-150">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e3490-151">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3490-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e3490-152">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e3490-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3490-153">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e3490-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e3490-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3490-154">RELATED LINKS</span></span>

