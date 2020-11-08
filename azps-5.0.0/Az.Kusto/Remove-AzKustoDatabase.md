---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278976"
---
# <span data-ttu-id="c68a1-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c68a1-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="c68a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c68a1-103">Verilen ada sahip veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="c68a1-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="c68a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c68a1-104">SYNTAX</span></span>

### <span data-ttu-id="c68a1-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c68a1-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c68a1-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="c68a1-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c68a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c68a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c68a1-108">Verilen ada sahip veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="c68a1-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="c68a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c68a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c68a1-110">Örnek 1: varolan bir kusto veritabanını adla silme</span><span class="sxs-lookup"><span data-stu-id="c68a1-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="c68a1-111">Yukarıdaki komut, "mykustodatabase" adlı kusto veritabanını "testrg" kaynak grubunda bulunan "testnewkustocluster" kümesinde siler.</span><span class="sxs-lookup"><span data-stu-id="c68a1-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c68a1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c68a1-112">PARAMETERS</span></span>

### <span data-ttu-id="c68a1-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="c68a1-113">-AsJob</span></span>
<span data-ttu-id="c68a1-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="c68a1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c68a1-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c68a1-115">-ClusterName</span></span>
<span data-ttu-id="c68a1-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c68a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68a1-117">-DefaultProfile</span></span>
<span data-ttu-id="c68a1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c68a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c68a1-119">-InputObject</span></span>
<span data-ttu-id="c68a1-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c68a1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c68a1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c68a1-121">-Name</span></span>
<span data-ttu-id="c68a1-122">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68a1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c68a1-123">-NoWait</span></span>
<span data-ttu-id="c68a1-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="c68a1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c68a1-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c68a1-125">-PassThru</span></span>
<span data-ttu-id="c68a1-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="c68a1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c68a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="c68a1-128">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c68a1-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c68a1-129">-SubscriptionId</span></span>
<span data-ttu-id="c68a1-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c68a1-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c68a1-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c68a1-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c68a1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c68a1-132">-Confirm</span></span>
<span data-ttu-id="c68a1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c68a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68a1-134">-WhatIf</span></span>
<span data-ttu-id="c68a1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c68a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68a1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c68a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68a1-137">CommonParameters</span></span>
<span data-ttu-id="c68a1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c68a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68a1-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c68a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68a1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c68a1-140">INPUTS</span></span>

### <span data-ttu-id="c68a1-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="c68a1-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c68a1-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c68a1-142">OUTPUTS</span></span>

### <span data-ttu-id="c68a1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c68a1-143">System.Boolean</span></span>

## <span data-ttu-id="c68a1-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c68a1-144">NOTES</span></span>

<span data-ttu-id="c68a1-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c68a1-145">ALIASES</span></span>

<span data-ttu-id="c68a1-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c68a1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c68a1-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c68a1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c68a1-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c68a1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c68a1-149">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="c68a1-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c68a1-150">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c68a1-151">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c68a1-152">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c68a1-153">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c68a1-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="c68a1-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c68a1-155">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="c68a1-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c68a1-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c68a1-157">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c68a1-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c68a1-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c68a1-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c68a1-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c68a1-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c68a1-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c68a1-160">RELATED LINKS</span></span>

