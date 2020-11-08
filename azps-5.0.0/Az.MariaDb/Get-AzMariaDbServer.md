---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278904"
---
# <span data-ttu-id="a330d-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="a330d-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="a330d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a330d-102">SYNOPSIS</span></span>
<span data-ttu-id="a330d-103">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a330d-103">Gets information about a server.</span></span>

## <span data-ttu-id="a330d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a330d-104">SYNTAX</span></span>

### <span data-ttu-id="a330d-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a330d-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a330d-106">Al</span><span class="sxs-lookup"><span data-stu-id="a330d-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a330d-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a330d-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a330d-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="a330d-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a330d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a330d-109">DESCRIPTION</span></span>
<span data-ttu-id="a330d-110">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a330d-110">Gets information about a server.</span></span>

## <span data-ttu-id="a330d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a330d-111">EXAMPLES</span></span>

### <span data-ttu-id="a330d-112">Örnek 1: abonelikler altındaki tüm Marilıst</span><span class="sxs-lookup"><span data-stu-id="a330d-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="a330d-113">Bu komut, aboneliklerin altındaki tüm Marilistesini listeler.</span><span class="sxs-lookup"><span data-stu-id="a330d-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="a330d-114">Örnek 2: kaynak grubu altındaki tüm Marilıst</span><span class="sxs-lookup"><span data-stu-id="a330d-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="a330d-115">Bu komut, kaynak grubu altındaki tüm Marilisteler.</span><span class="sxs-lookup"><span data-stu-id="a330d-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="a330d-116">Örnek 3: MariaDB alın</span><span class="sxs-lookup"><span data-stu-id="a330d-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="a330d-117">Bu komut bir MariaDB alır.</span><span class="sxs-lookup"><span data-stu-id="a330d-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="a330d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a330d-118">PARAMETERS</span></span>

### <span data-ttu-id="a330d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a330d-119">-DefaultProfile</span></span>
<span data-ttu-id="a330d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a330d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a330d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a330d-121">-InputObject</span></span>
<span data-ttu-id="a330d-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a330d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a330d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a330d-123">-Name</span></span>
<span data-ttu-id="a330d-124">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-124">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a330d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a330d-125">-ResourceGroupName</span></span>
<span data-ttu-id="a330d-126">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a330d-127">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a330d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a330d-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a330d-128">-SubscriptionId</span></span>
<span data-ttu-id="a330d-129">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a330d-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a330d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a330d-130">CommonParameters</span></span>
<span data-ttu-id="a330d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a330d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a330d-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a330d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a330d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a330d-133">INPUTS</span></span>

### <span data-ttu-id="a330d-134">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="a330d-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a330d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a330d-135">OUTPUTS</span></span>

### <span data-ttu-id="a330d-136">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="a330d-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="a330d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a330d-137">NOTES</span></span>

<span data-ttu-id="a330d-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a330d-138">ALIASES</span></span>

<span data-ttu-id="a330d-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a330d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a330d-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a330d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a330d-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a330d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a330d-142">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a330d-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a330d-143">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a330d-144">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a330d-145">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a330d-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a330d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a330d-147">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a330d-148">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a330d-149">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a330d-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a330d-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a330d-151">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a330d-152">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a330d-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a330d-153">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="a330d-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a330d-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a330d-154">RELATED LINKS</span></span>

