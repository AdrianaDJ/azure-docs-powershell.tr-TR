---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278981"
---
# <span data-ttu-id="504ca-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="504ca-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="504ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504ca-102">SYNOPSIS</span></span>
<span data-ttu-id="504ca-103">Kusto küme principalAssignment siler.</span><span class="sxs-lookup"><span data-stu-id="504ca-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="504ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="504ca-104">SYNTAX</span></span>

### <span data-ttu-id="504ca-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="504ca-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="504ca-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="504ca-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="504ca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="504ca-107">DESCRIPTION</span></span>
<span data-ttu-id="504ca-108">Kusto küme principalAssignment siler.</span><span class="sxs-lookup"><span data-stu-id="504ca-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="504ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="504ca-109">EXAMPLES</span></span>

### <span data-ttu-id="504ca-110">Örnek 1: varolan bir kusto kümesini ada göre silme</span><span class="sxs-lookup"><span data-stu-id="504ca-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="504ca-111">Yukarıdaki komut kusto kümesinde "kustoprincipal1" adlı PrincipalAssignment siler.</span><span class="sxs-lookup"><span data-stu-id="504ca-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="504ca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="504ca-112">PARAMETERS</span></span>

### <span data-ttu-id="504ca-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="504ca-113">-AsJob</span></span>
<span data-ttu-id="504ca-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="504ca-114">Run the command as a job</span></span>

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

### <span data-ttu-id="504ca-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="504ca-115">-ClusterName</span></span>
<span data-ttu-id="504ca-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504ca-117">-DefaultProfile</span></span>
<span data-ttu-id="504ca-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="504ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="504ca-119">-InputObject</span></span>
<span data-ttu-id="504ca-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="504ca-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="504ca-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="504ca-121">-NoWait</span></span>
<span data-ttu-id="504ca-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="504ca-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="504ca-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="504ca-123">-PassThru</span></span>
<span data-ttu-id="504ca-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="504ca-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="504ca-125">-Princıpalassignmentname</span><span class="sxs-lookup"><span data-stu-id="504ca-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="504ca-126">Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-126">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="504ca-128">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ca-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="504ca-129">-SubscriptionId</span></span>
<span data-ttu-id="504ca-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="504ca-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="504ca-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="504ca-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504ca-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="504ca-132">-Confirm</span></span>
<span data-ttu-id="504ca-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="504ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="504ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504ca-134">-WhatIf</span></span>
<span data-ttu-id="504ca-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="504ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="504ca-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="504ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="504ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504ca-137">CommonParameters</span></span>
<span data-ttu-id="504ca-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="504ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504ca-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="504ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504ca-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="504ca-140">INPUTS</span></span>

### <span data-ttu-id="504ca-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="504ca-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="504ca-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="504ca-142">OUTPUTS</span></span>

### <span data-ttu-id="504ca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="504ca-143">System.Boolean</span></span>

## <span data-ttu-id="504ca-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="504ca-144">NOTES</span></span>

<span data-ttu-id="504ca-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="504ca-145">ALIASES</span></span>

<span data-ttu-id="504ca-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="504ca-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="504ca-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="504ca-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="504ca-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="504ca-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="504ca-149">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="504ca-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="504ca-150">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="504ca-151">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="504ca-152">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="504ca-153">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="504ca-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="504ca-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="504ca-155">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="504ca-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="504ca-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="504ca-157">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="504ca-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="504ca-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="504ca-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="504ca-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="504ca-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="504ca-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="504ca-160">RELATED LINKS</span></span>

