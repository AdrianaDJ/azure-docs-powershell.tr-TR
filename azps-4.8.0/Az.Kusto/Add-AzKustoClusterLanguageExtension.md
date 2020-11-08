---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267341"
---
# <span data-ttu-id="b4412-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="b4412-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="b4412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4412-102">SYNOPSIS</span></span>
<span data-ttu-id="b4412-103">KQL sorgularında çalıştırılabilecek dil uzantılarının listesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b4412-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b4412-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4412-104">SYNTAX</span></span>

### <span data-ttu-id="b4412-105">AddExpanded (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4412-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4412-106">Addviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="b4412-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4412-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4412-107">DESCRIPTION</span></span>
<span data-ttu-id="b4412-108">KQL sorgularında çalıştırılabilecek dil uzantılarının listesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b4412-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b4412-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4412-109">EXAMPLES</span></span>

### <span data-ttu-id="b4412-110">Örnek 1: dil uzantılarının listesini ekleme</span><span class="sxs-lookup"><span data-stu-id="b4412-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="b4412-111">Yukarıdaki komut, KQL sorgularında çalıştırılabilecek dil uzantılarının listesini ekler</span><span class="sxs-lookup"><span data-stu-id="b4412-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="b4412-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4412-112">PARAMETERS</span></span>

### <span data-ttu-id="b4412-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4412-113">-AsJob</span></span>
<span data-ttu-id="b4412-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="b4412-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b4412-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b4412-115">-ClusterName</span></span>
<span data-ttu-id="b4412-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4412-117">-DefaultProfile</span></span>
<span data-ttu-id="b4412-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4412-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4412-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4412-119">-InputObject</span></span>
<span data-ttu-id="b4412-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4412-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4412-121">-NoWait</span></span>
<span data-ttu-id="b4412-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="b4412-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b4412-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b4412-123">-PassThru</span></span>
<span data-ttu-id="b4412-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="b4412-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b4412-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4412-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4412-126">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b4412-127">-SubscriptionId</span></span>
<span data-ttu-id="b4412-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b4412-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b4412-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b4412-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-130">-Değer</span><span class="sxs-lookup"><span data-stu-id="b4412-130">-Value</span></span>
<span data-ttu-id="b4412-131">Dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="b4412-131">The list of language extensions.</span></span>
<span data-ttu-id="b4412-132">Oluşturmak için, değer özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b4412-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4412-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4412-133">-Confirm</span></span>
<span data-ttu-id="b4412-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4412-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4412-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4412-135">-WhatIf</span></span>
<span data-ttu-id="b4412-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4412-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4412-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4412-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4412-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4412-138">CommonParameters</span></span>
<span data-ttu-id="b4412-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4412-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4412-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4412-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4412-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4412-141">INPUTS</span></span>

### <span data-ttu-id="b4412-142">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="b4412-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b4412-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4412-143">OUTPUTS</span></span>

### <span data-ttu-id="b4412-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4412-144">System.Boolean</span></span>

## <span data-ttu-id="b4412-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4412-145">NOTES</span></span>

<span data-ttu-id="b4412-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b4412-146">ALIASES</span></span>

<span data-ttu-id="b4412-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b4412-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4412-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b4412-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4412-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4412-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4412-150">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b4412-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4412-151">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b4412-152">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b4412-153">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b4412-154">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b4412-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b4412-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4412-156">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="b4412-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b4412-157">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b4412-158">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b4412-159">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b4412-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b4412-160">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b4412-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b4412-161">DEĞER <ılanguageextension [] >: dil uzantılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="b4412-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="b4412-162">`[Name <LanguageExtensionName?>]`: Dil uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="b4412-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="b4412-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4412-163">RELATED LINKS</span></span>

