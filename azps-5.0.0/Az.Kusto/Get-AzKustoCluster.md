---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279022"
---
# <span data-ttu-id="c3ac7-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c3ac7-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="c3ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ac7-103">Kusto kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="c3ac7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3ac7-104">SYNTAX</span></span>

### <span data-ttu-id="c3ac7-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3ac7-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c3ac7-106">Al</span><span class="sxs-lookup"><span data-stu-id="c3ac7-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c3ac7-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c3ac7-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c3ac7-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="c3ac7-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3ac7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3ac7-109">DESCRIPTION</span></span>
<span data-ttu-id="c3ac7-110">Kusto kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="c3ac7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3ac7-111">EXAMPLES</span></span>

### <span data-ttu-id="c3ac7-112">Örnek 1: kaynak grubundaki tüm kusto kümelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="c3ac7-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="c3ac7-113">Yukarıdaki komut, "testrg" kaynak grubundaki tüm kusto kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="c3ac7-114">Örnek 2: adla belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="c3ac7-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="c3ac7-115">Yukarıdaki komut, "testrg" kaynak grubunda "testnewkustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="c3ac7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3ac7-116">PARAMETERS</span></span>

### <span data-ttu-id="c3ac7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ac7-117">-DefaultProfile</span></span>
<span data-ttu-id="c3ac7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3ac7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3ac7-119">-InputObject</span></span>
<span data-ttu-id="c3ac7-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c3ac7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3ac7-121">-Name</span></span>
<span data-ttu-id="c3ac7-122">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ac7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ac7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3ac7-124">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c3ac7-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c3ac7-125">-SubscriptionId</span></span>
<span data-ttu-id="c3ac7-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c3ac7-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ac7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ac7-128">CommonParameters</span></span>
<span data-ttu-id="c3ac7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ac7-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ac7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3ac7-131">INPUTS</span></span>

### <span data-ttu-id="c3ac7-132">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="c3ac7-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c3ac7-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3ac7-133">OUTPUTS</span></span>

### <span data-ttu-id="c3ac7-134">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıluster</span><span class="sxs-lookup"><span data-stu-id="c3ac7-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="c3ac7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3ac7-135">NOTES</span></span>

<span data-ttu-id="c3ac7-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c3ac7-136">ALIASES</span></span>

<span data-ttu-id="c3ac7-137">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c3ac7-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3ac7-138">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3ac7-139">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3ac7-140">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c3ac7-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3ac7-141">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c3ac7-142">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c3ac7-143">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c3ac7-144">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c3ac7-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c3ac7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3ac7-146">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c3ac7-147">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c3ac7-148">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c3ac7-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c3ac7-150">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c3ac7-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c3ac7-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3ac7-151">RELATED LINKS</span></span>

