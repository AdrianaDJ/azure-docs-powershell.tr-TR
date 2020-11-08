---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267176"
---
# <span data-ttu-id="13301-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="13301-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="13301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13301-102">SYNOPSIS</span></span>
<span data-ttu-id="13301-103">Kusto kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="13301-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="13301-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13301-104">SYNTAX</span></span>

### <span data-ttu-id="13301-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13301-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13301-106">Al</span><span class="sxs-lookup"><span data-stu-id="13301-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13301-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="13301-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13301-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="13301-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="13301-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="13301-109">DESCRIPTION</span></span>
<span data-ttu-id="13301-110">Kusto kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="13301-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="13301-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13301-111">EXAMPLES</span></span>

### <span data-ttu-id="13301-112">Örnek 1: kaynak grubundaki tüm kusto kümelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="13301-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="13301-113">Yukarıdaki komut, "testrg" kaynak grubundaki tüm kusto kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="13301-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="13301-114">Örnek 2: adla belirli bir kusto kümesi edinme</span><span class="sxs-lookup"><span data-stu-id="13301-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="13301-115">Yukarıdaki komut, "testrg" kaynak grubunda "testnewkustocluster" adlı kusto kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="13301-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="13301-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13301-116">PARAMETERS</span></span>

### <span data-ttu-id="13301-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13301-117">-DefaultProfile</span></span>
<span data-ttu-id="13301-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13301-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13301-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13301-119">-InputObject</span></span>
<span data-ttu-id="13301-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13301-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13301-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="13301-121">-Name</span></span>
<span data-ttu-id="13301-122">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="13301-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="13301-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13301-123">-ResourceGroupName</span></span>
<span data-ttu-id="13301-124">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="13301-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="13301-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="13301-125">-SubscriptionId</span></span>
<span data-ttu-id="13301-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="13301-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="13301-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="13301-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="13301-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13301-128">CommonParameters</span></span>
<span data-ttu-id="13301-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13301-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13301-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13301-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13301-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13301-131">INPUTS</span></span>

### <span data-ttu-id="13301-132">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="13301-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="13301-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13301-133">OUTPUTS</span></span>

### <span data-ttu-id="13301-134">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıluster</span><span class="sxs-lookup"><span data-stu-id="13301-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="13301-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13301-135">NOTES</span></span>

<span data-ttu-id="13301-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="13301-136">ALIASES</span></span>

<span data-ttu-id="13301-137">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="13301-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13301-138">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="13301-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13301-139">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13301-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13301-140">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="13301-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13301-141">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="13301-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="13301-142">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="13301-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="13301-143">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="13301-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="13301-144">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="13301-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="13301-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="13301-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13301-146">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="13301-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="13301-147">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="13301-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="13301-148">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="13301-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="13301-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="13301-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="13301-150">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="13301-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="13301-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13301-151">RELATED LINKS</span></span>

