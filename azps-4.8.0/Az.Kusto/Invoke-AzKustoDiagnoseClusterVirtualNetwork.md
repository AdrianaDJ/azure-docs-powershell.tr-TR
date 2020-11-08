---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273552"
---
# <span data-ttu-id="1fc7f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1fc7f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="1fc7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc7f-103">Hizmetin bağımlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="1fc7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fc7f-104">SYNTAX</span></span>

### <span data-ttu-id="1fc7f-105">Tanıla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1fc7f-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1fc7f-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fc7f-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fc7f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fc7f-107">DESCRIPTION</span></span>
<span data-ttu-id="1fc7f-108">Hizmetin bağımlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="1fc7f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fc7f-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc7f-110">Örnek 1: dış kaynaklar için ağ bağlantısı tanılaması 'nı göster</span><span class="sxs-lookup"><span data-stu-id="1fc7f-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="1fc7f-111">Yukarıdaki komut, "testnewkustocluster" kümesinin bağlı olduğu dış kaynaklar için ağ bağlantısı durumunu tanılar</span><span class="sxs-lookup"><span data-stu-id="1fc7f-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="1fc7f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fc7f-112">PARAMETERS</span></span>

### <span data-ttu-id="1fc7f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1fc7f-113">-AsJob</span></span>
<span data-ttu-id="1fc7f-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1fc7f-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1fc7f-115">-ClusterName</span></span>
<span data-ttu-id="1fc7f-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc7f-117">-DefaultProfile</span></span>
<span data-ttu-id="1fc7f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fc7f-119">-InputObject</span></span>
<span data-ttu-id="1fc7f-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fc7f-121">-NoWait</span></span>
<span data-ttu-id="1fc7f-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1fc7f-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1fc7f-124">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1fc7f-125">-SubscriptionId</span></span>
<span data-ttu-id="1fc7f-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fc7f-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc7f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1fc7f-128">-Confirm</span></span>
<span data-ttu-id="1fc7f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc7f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc7f-130">-WhatIf</span></span>
<span data-ttu-id="1fc7f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc7f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc7f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc7f-133">CommonParameters</span></span>
<span data-ttu-id="1fc7f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc7f-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc7f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fc7f-136">INPUTS</span></span>

### <span data-ttu-id="1fc7f-137">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="1fc7f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1fc7f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fc7f-138">OUTPUTS</span></span>

### <span data-ttu-id="1fc7f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc7f-139">System.String</span></span>

## <span data-ttu-id="1fc7f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fc7f-140">NOTES</span></span>

<span data-ttu-id="1fc7f-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1fc7f-141">ALIASES</span></span>

<span data-ttu-id="1fc7f-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1fc7f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fc7f-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fc7f-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fc7f-145">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1fc7f-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fc7f-146">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1fc7f-147">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1fc7f-148">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1fc7f-149">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1fc7f-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1fc7f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fc7f-151">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1fc7f-152">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1fc7f-153">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1fc7f-154">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fc7f-155">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1fc7f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fc7f-156">RELATED LINKS</span></span>

