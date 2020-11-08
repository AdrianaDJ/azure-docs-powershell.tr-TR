---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280180"
---
# <span data-ttu-id="ba287-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ba287-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="ba287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba287-102">SYNOPSIS</span></span>
<span data-ttu-id="ba287-103">Küme adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ba287-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="ba287-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba287-104">SYNTAX</span></span>

### <span data-ttu-id="ba287-105">Onay genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba287-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba287-106">Checkviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="ba287-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba287-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba287-107">DESCRIPTION</span></span>
<span data-ttu-id="ba287-108">Küme adının geçerli olduğunu ve kullanımda olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="ba287-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="ba287-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba287-109">EXAMPLES</span></span>

### <span data-ttu-id="ba287-110">Örnek 1: kullanımda olan bir kusto küme adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="ba287-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="ba287-111">Yukarıdaki komut, "testnewkustocluster" adlı kusto kümesinin "Doğu US" bölgesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba287-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="ba287-112">Örnek 2: kullanımda olmayan bir kusto küme adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="ba287-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ba287-113">Yukarıdaki komut, "availablekustocluster" adlı kusto kümesinin "Doğu US" bölgesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba287-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="ba287-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba287-114">PARAMETERS</span></span>

### <span data-ttu-id="ba287-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba287-115">-DefaultProfile</span></span>
<span data-ttu-id="ba287-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba287-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba287-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba287-117">-InputObject</span></span>
<span data-ttu-id="ba287-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba287-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba287-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="ba287-119">-Location</span></span>
<span data-ttu-id="ba287-120">Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ba287-120">Azure location.</span></span>

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

### <span data-ttu-id="ba287-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba287-121">-Name</span></span>
<span data-ttu-id="ba287-122">Küme adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-122">Cluster name.</span></span>

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

### <span data-ttu-id="ba287-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ba287-123">-SubscriptionId</span></span>
<span data-ttu-id="ba287-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba287-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba287-125">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ba287-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba287-126">-Tür</span><span class="sxs-lookup"><span data-stu-id="ba287-126">-Type</span></span>
<span data-ttu-id="ba287-127">Kaynak türü olan Microsoft. kusto/kümeler.</span><span class="sxs-lookup"><span data-stu-id="ba287-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="ba287-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba287-128">-Confirm</span></span>
<span data-ttu-id="ba287-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba287-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba287-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba287-130">-WhatIf</span></span>
<span data-ttu-id="ba287-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba287-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba287-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba287-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba287-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba287-133">CommonParameters</span></span>
<span data-ttu-id="ba287-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba287-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba287-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba287-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba287-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba287-136">INPUTS</span></span>

### <span data-ttu-id="ba287-137">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="ba287-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ba287-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba287-138">OUTPUTS</span></span>

### <span data-ttu-id="ba287-139">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ba287-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ba287-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba287-140">NOTES</span></span>

<span data-ttu-id="ba287-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ba287-141">ALIASES</span></span>

<span data-ttu-id="ba287-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ba287-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba287-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba287-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba287-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba287-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba287-145">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ba287-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba287-146">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ba287-147">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ba287-148">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ba287-149">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ba287-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ba287-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba287-151">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ba287-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ba287-152">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ba287-153">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba287-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ba287-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba287-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ba287-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ba287-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba287-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba287-156">RELATED LINKS</span></span>

