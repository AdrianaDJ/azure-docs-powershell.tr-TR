---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108215"
---
# <span data-ttu-id="1fd33-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1fd33-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="1fd33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd33-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd33-103">Verilen adla veri bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="1fd33-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="1fd33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fd33-104">SYNTAX</span></span>

### <span data-ttu-id="1fd33-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1fd33-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fd33-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1fd33-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fd33-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fd33-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd33-108">Verilen adla veri bağlantısını siler.</span><span class="sxs-lookup"><span data-stu-id="1fd33-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="1fd33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fd33-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd33-110">Örnek 1: varolan bir veri bağlantısını adla silme</span><span class="sxs-lookup"><span data-stu-id="1fd33-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="1fd33-111">Yukarıdaki komut, "mykustodataconnection" adlı "mykustodatabase" veritabanındaki "" adlı veri bağlantısını, "testrg" kaynak grubunda bulundu</span><span class="sxs-lookup"><span data-stu-id="1fd33-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="1fd33-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fd33-112">PARAMETERS</span></span>

### <span data-ttu-id="1fd33-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1fd33-113">-AsJob</span></span>
<span data-ttu-id="1fd33-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1fd33-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1fd33-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1fd33-115">-ClusterName</span></span>
<span data-ttu-id="1fd33-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fd33-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fd33-117">-DatabaseName</span></span>
<span data-ttu-id="1fd33-118">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fd33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd33-119">-DefaultProfile</span></span>
<span data-ttu-id="1fd33-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fd33-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd33-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fd33-121">-InputObject</span></span>
<span data-ttu-id="1fd33-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fd33-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fd33-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1fd33-123">-Name</span></span>
<span data-ttu-id="1fd33-124">Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd33-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fd33-125">-NoWait</span></span>
<span data-ttu-id="1fd33-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1fd33-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1fd33-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1fd33-127">-PassThru</span></span>
<span data-ttu-id="1fd33-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="1fd33-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1fd33-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd33-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fd33-130">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1fd33-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1fd33-131">-SubscriptionId</span></span>
<span data-ttu-id="1fd33-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1fd33-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fd33-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1fd33-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1fd33-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1fd33-134">-Confirm</span></span>
<span data-ttu-id="1fd33-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1fd33-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd33-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd33-136">-WhatIf</span></span>
<span data-ttu-id="1fd33-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1fd33-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd33-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1fd33-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd33-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd33-139">CommonParameters</span></span>
<span data-ttu-id="1fd33-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fd33-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd33-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fd33-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd33-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fd33-142">INPUTS</span></span>

### <span data-ttu-id="1fd33-143">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="1fd33-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1fd33-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fd33-144">OUTPUTS</span></span>

### <span data-ttu-id="1fd33-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fd33-145">System.Boolean</span></span>

## <span data-ttu-id="1fd33-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fd33-146">NOTES</span></span>

<span data-ttu-id="1fd33-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1fd33-147">ALIASES</span></span>

<span data-ttu-id="1fd33-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1fd33-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fd33-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fd33-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fd33-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fd33-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fd33-151">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1fd33-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fd33-152">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1fd33-153">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1fd33-154">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1fd33-155">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1fd33-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1fd33-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fd33-157">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="1fd33-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1fd33-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1fd33-159">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fd33-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1fd33-160">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1fd33-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fd33-161">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1fd33-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1fd33-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fd33-162">RELATED LINKS</span></span>

