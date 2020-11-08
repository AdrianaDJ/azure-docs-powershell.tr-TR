---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108213"
---
# <span data-ttu-id="f05c3-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f05c3-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f05c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f05c3-103">Kusto principalAssignment siler.</span><span class="sxs-lookup"><span data-stu-id="f05c3-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f05c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f05c3-104">SYNTAX</span></span>

### <span data-ttu-id="f05c3-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f05c3-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f05c3-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f05c3-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f05c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f05c3-107">DESCRIPTION</span></span>
<span data-ttu-id="f05c3-108">Kusto principalAssignment siler.</span><span class="sxs-lookup"><span data-stu-id="f05c3-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f05c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f05c3-109">EXAMPLES</span></span>

### <span data-ttu-id="f05c3-110">Örnek 1: varolan bir kusto veritabanını adla silme</span><span class="sxs-lookup"><span data-stu-id="f05c3-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="f05c3-111">Yukarıdaki komut kusto veritabanında "kustoprincipal1" adlı PrincipalAssignment öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="f05c3-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="f05c3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f05c3-112">PARAMETERS</span></span>

### <span data-ttu-id="f05c3-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f05c3-113">-AsJob</span></span>
<span data-ttu-id="f05c3-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f05c3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f05c3-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f05c3-115">-ClusterName</span></span>
<span data-ttu-id="f05c3-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f05c3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f05c3-117">-DatabaseName</span></span>
<span data-ttu-id="f05c3-118">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f05c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05c3-119">-DefaultProfile</span></span>
<span data-ttu-id="f05c3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f05c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05c3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f05c3-121">-InputObject</span></span>
<span data-ttu-id="f05c3-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f05c3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f05c3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f05c3-123">-NoWait</span></span>
<span data-ttu-id="f05c3-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f05c3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f05c3-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f05c3-125">-PassThru</span></span>
<span data-ttu-id="f05c3-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="f05c3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f05c3-127">-Princıpalassignmentname</span><span class="sxs-lookup"><span data-stu-id="f05c3-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f05c3-128">Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f05c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="f05c3-130">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f05c3-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f05c3-131">-SubscriptionId</span></span>
<span data-ttu-id="f05c3-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f05c3-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f05c3-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f05c3-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f05c3-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f05c3-134">-Confirm</span></span>
<span data-ttu-id="f05c3-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f05c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f05c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05c3-136">-WhatIf</span></span>
<span data-ttu-id="f05c3-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f05c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05c3-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f05c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f05c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05c3-139">CommonParameters</span></span>
<span data-ttu-id="f05c3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f05c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05c3-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f05c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05c3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f05c3-142">INPUTS</span></span>

### <span data-ttu-id="f05c3-143">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="f05c3-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f05c3-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f05c3-144">OUTPUTS</span></span>

### <span data-ttu-id="f05c3-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f05c3-145">System.Boolean</span></span>

## <span data-ttu-id="f05c3-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f05c3-146">NOTES</span></span>

<span data-ttu-id="f05c3-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f05c3-147">ALIASES</span></span>

<span data-ttu-id="f05c3-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f05c3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f05c3-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f05c3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f05c3-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f05c3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f05c3-151">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f05c3-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f05c3-152">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f05c3-153">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f05c3-154">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f05c3-155">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f05c3-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f05c3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f05c3-157">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="f05c3-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f05c3-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f05c3-159">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f05c3-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f05c3-160">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f05c3-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f05c3-161">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f05c3-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f05c3-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f05c3-162">RELATED LINKS</span></span>

