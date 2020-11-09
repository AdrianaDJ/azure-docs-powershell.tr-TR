---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323875"
---
# <span data-ttu-id="34ae3-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="34ae3-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="34ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="34ae3-103">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-103">Gets information about a server.</span></span>

## <span data-ttu-id="34ae3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34ae3-104">SYNTAX</span></span>

### <span data-ttu-id="34ae3-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34ae3-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34ae3-106">Al</span><span class="sxs-lookup"><span data-stu-id="34ae3-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34ae3-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="34ae3-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34ae3-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="34ae3-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="34ae3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ae3-109">DESCRIPTION</span></span>
<span data-ttu-id="34ae3-110">Sunucu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-110">Gets information about a server.</span></span>

## <span data-ttu-id="34ae3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34ae3-111">EXAMPLES</span></span>

### <span data-ttu-id="34ae3-112">Örnek 1: varsayılan içerikle MySql sunucusu edinin</span><span class="sxs-lookup"><span data-stu-id="34ae3-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="34ae3-113">Bu cmdlet, MySql sunucusunu varsayılan içerikle alır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="34ae3-114">Örnek 2: kaynak grubuna göre MySql sunucusunu ve sunucu adını alın</span><span class="sxs-lookup"><span data-stu-id="34ae3-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="34ae3-115">Bu cmdlet, kaynak grubu ve sunucu adına göre MySql sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="34ae3-116">Örnek 3: belirtilen kaynak grubundaki tüm MySql sunucularını listeler</span><span class="sxs-lookup"><span data-stu-id="34ae3-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="34ae3-117">Bu cmdlet, belirtilen kaynak grubundaki tüm MySql sunucularını listeler.</span><span class="sxs-lookup"><span data-stu-id="34ae3-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="34ae3-118">Örnek 4: kimliğe göre MySql sunucusunu alma</span><span class="sxs-lookup"><span data-stu-id="34ae3-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="34ae3-119">Bu cmdlet listeleri, MySql sunucusunu kimliğe göre alır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="34ae3-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34ae3-120">PARAMETERS</span></span>

### <span data-ttu-id="34ae3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ae3-121">-DefaultProfile</span></span>
<span data-ttu-id="34ae3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34ae3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ae3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34ae3-123">-InputObject</span></span>
<span data-ttu-id="34ae3-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34ae3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ae3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="34ae3-125">-Name</span></span>
<span data-ttu-id="34ae3-126">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-126">The name of the server.</span></span>

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

### <span data-ttu-id="34ae3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ae3-127">-ResourceGroupName</span></span>
<span data-ttu-id="34ae3-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-128">The name of the resource group.</span></span>
<span data-ttu-id="34ae3-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34ae3-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="34ae3-130">-SubscriptionId</span></span>
<span data-ttu-id="34ae3-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34ae3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34ae3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ae3-132">CommonParameters</span></span>
<span data-ttu-id="34ae3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34ae3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ae3-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34ae3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ae3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34ae3-135">INPUTS</span></span>

### <span data-ttu-id="34ae3-136">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="34ae3-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="34ae3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34ae3-137">OUTPUTS</span></span>

### <span data-ttu-id="34ae3-138">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="34ae3-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="34ae3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34ae3-139">NOTES</span></span>

<span data-ttu-id="34ae3-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="34ae3-140">ALIASES</span></span>

<span data-ttu-id="34ae3-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="34ae3-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34ae3-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="34ae3-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34ae3-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34ae3-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34ae3-144">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="34ae3-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34ae3-145">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="34ae3-146">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="34ae3-147">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="34ae3-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="34ae3-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34ae3-149">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="34ae3-150">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34ae3-151">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="34ae3-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="34ae3-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="34ae3-153">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="34ae3-154">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34ae3-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34ae3-155">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="34ae3-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="34ae3-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34ae3-156">RELATED LINKS</span></span>

