---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279031"
---
# <span data-ttu-id="61de3-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="61de3-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="61de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61de3-102">SYNOPSIS</span></span>
<span data-ttu-id="61de3-103">Veritabanı sorumlusu izinleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="61de3-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="61de3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61de3-104">SYNTAX</span></span>

### <span data-ttu-id="61de3-105">AddExpanded (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61de3-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="61de3-106">Addviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="61de3-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="61de3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="61de3-107">DESCRIPTION</span></span>
<span data-ttu-id="61de3-108">Veritabanı sorumlusu izinleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="61de3-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="61de3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61de3-109">EXAMPLES</span></span>

### <span data-ttu-id="61de3-110">Örnek 1: veritabanı sorumluları izinlerini ekleme</span><span class="sxs-lookup"><span data-stu-id="61de3-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="61de3-111">Yukarıdaki komut veritabanı sorumlusu izinlerini ekler</span><span class="sxs-lookup"><span data-stu-id="61de3-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="61de3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61de3-112">PARAMETERS</span></span>

### <span data-ttu-id="61de3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61de3-113">-ClusterName</span></span>
<span data-ttu-id="61de3-114">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="61de3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61de3-115">-DatabaseName</span></span>
<span data-ttu-id="61de3-116">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="61de3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61de3-117">-DefaultProfile</span></span>
<span data-ttu-id="61de3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61de3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61de3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61de3-119">-InputObject</span></span>
<span data-ttu-id="61de3-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61de3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61de3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61de3-121">-ResourceGroupName</span></span>
<span data-ttu-id="61de3-122">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="61de3-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="61de3-123">-SubscriptionId</span></span>
<span data-ttu-id="61de3-124">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="61de3-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="61de3-125">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="61de3-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="61de3-126">-Değer</span><span class="sxs-lookup"><span data-stu-id="61de3-126">-Value</span></span>
<span data-ttu-id="61de3-127">Kusto veritabanı sorumlularının listesi.</span><span class="sxs-lookup"><span data-stu-id="61de3-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="61de3-128">Oluşturmak için, değer özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61de3-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61de3-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="61de3-129">-Confirm</span></span>
<span data-ttu-id="61de3-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61de3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61de3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61de3-131">-WhatIf</span></span>
<span data-ttu-id="61de3-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61de3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61de3-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61de3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61de3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61de3-134">CommonParameters</span></span>
<span data-ttu-id="61de3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61de3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61de3-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61de3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61de3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61de3-137">INPUTS</span></span>

### <span data-ttu-id="61de3-138">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="61de3-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="61de3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61de3-139">OUTPUTS</span></span>

### <span data-ttu-id="61de3-140">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="61de3-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="61de3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61de3-141">NOTES</span></span>

<span data-ttu-id="61de3-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="61de3-142">ALIASES</span></span>

<span data-ttu-id="61de3-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="61de3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61de3-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61de3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61de3-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61de3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61de3-146">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="61de3-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61de3-147">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="61de3-148">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="61de3-149">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="61de3-150">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="61de3-151">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="61de3-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61de3-152">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="61de3-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="61de3-153">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="61de3-154">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="61de3-155">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="61de3-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="61de3-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="61de3-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="61de3-157">DEĞER <IDatabasePrincipal [] >: kusto veritabanı sorumlularının listesi.</span><span class="sxs-lookup"><span data-stu-id="61de3-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="61de3-158">`Name <String>`: Veritabanı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="61de3-159">`Role <DatabasePrincipalRole>`: Veritabanı sorumlusu rolü.</span><span class="sxs-lookup"><span data-stu-id="61de3-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="61de3-160">`Type <DatabasePrincipalType>`: Veritabanı sorumlusu türü.</span><span class="sxs-lookup"><span data-stu-id="61de3-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="61de3-161">`[AppId <String>]`: Uygulama kimliği-yalnızca uygulama sorumlusu türü için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="61de3-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="61de3-162">`[Email <String>]`: Varsa, veritabanı sorumlusu e-postası.</span><span class="sxs-lookup"><span data-stu-id="61de3-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="61de3-163">`[Fqn <String>]`: Veritabanı sorumlusu tam adı.</span><span class="sxs-lookup"><span data-stu-id="61de3-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="61de3-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61de3-164">RELATED LINKS</span></span>

