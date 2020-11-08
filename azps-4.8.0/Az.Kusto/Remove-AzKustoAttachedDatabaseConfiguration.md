---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108219"
---
# <span data-ttu-id="129e9-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="129e9-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="129e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="129e9-102">SYNOPSIS</span></span>
<span data-ttu-id="129e9-103">Eklenen veritabanı yapılandırmasını verilen adla siler.</span><span class="sxs-lookup"><span data-stu-id="129e9-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="129e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="129e9-104">SYNTAX</span></span>

### <span data-ttu-id="129e9-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="129e9-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="129e9-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="129e9-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="129e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="129e9-107">DESCRIPTION</span></span>
<span data-ttu-id="129e9-108">Eklenen veritabanı yapılandırmasını verilen adla siler.</span><span class="sxs-lookup"><span data-stu-id="129e9-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="129e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="129e9-109">EXAMPLES</span></span>

### <span data-ttu-id="129e9-110">Örnek 1: var olan AttachedDatabaseConfiguration 'ı adıyla silme</span><span class="sxs-lookup"><span data-stu-id="129e9-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="129e9-111">Yukarıdaki komut, [testnewkustoclusterf "kümesinden AttachedDatabaseConfiguration" myizleme "dizininde tanımlanan izleme veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="129e9-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="129e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="129e9-112">PARAMETERS</span></span>

### <span data-ttu-id="129e9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="129e9-113">-AsJob</span></span>
<span data-ttu-id="129e9-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="129e9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="129e9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="129e9-115">-ClusterName</span></span>
<span data-ttu-id="129e9-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="129e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129e9-117">-DefaultProfile</span></span>
<span data-ttu-id="129e9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="129e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="129e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="129e9-119">-InputObject</span></span>
<span data-ttu-id="129e9-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="129e9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="129e9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="129e9-121">-Name</span></span>
<span data-ttu-id="129e9-122">Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="129e9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="129e9-123">-NoWait</span></span>
<span data-ttu-id="129e9-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="129e9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="129e9-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="129e9-125">-PassThru</span></span>
<span data-ttu-id="129e9-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="129e9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="129e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="129e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="129e9-128">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="129e9-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="129e9-129">-SubscriptionId</span></span>
<span data-ttu-id="129e9-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="129e9-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="129e9-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="129e9-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="129e9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="129e9-132">-Confirm</span></span>
<span data-ttu-id="129e9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="129e9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="129e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="129e9-134">-WhatIf</span></span>
<span data-ttu-id="129e9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="129e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="129e9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="129e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="129e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129e9-137">CommonParameters</span></span>
<span data-ttu-id="129e9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="129e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129e9-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="129e9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129e9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="129e9-140">INPUTS</span></span>

### <span data-ttu-id="129e9-141">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="129e9-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="129e9-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="129e9-142">OUTPUTS</span></span>

### <span data-ttu-id="129e9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="129e9-143">System.Boolean</span></span>

## <span data-ttu-id="129e9-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="129e9-144">NOTES</span></span>

<span data-ttu-id="129e9-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="129e9-145">ALIASES</span></span>

<span data-ttu-id="129e9-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="129e9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="129e9-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="129e9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="129e9-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="129e9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="129e9-149">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="129e9-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="129e9-150">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="129e9-151">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="129e9-152">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="129e9-153">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="129e9-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="129e9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="129e9-155">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="129e9-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="129e9-156">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="129e9-157">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="129e9-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="129e9-158">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="129e9-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="129e9-159">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="129e9-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="129e9-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="129e9-160">RELATED LINKS</span></span>

