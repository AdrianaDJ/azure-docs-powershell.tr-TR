---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265823"
---
# <span data-ttu-id="b1738-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="b1738-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="b1738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1738-102">SYNOPSIS</span></span>
<span data-ttu-id="b1738-103">Sunucuyu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b1738-103">Restarts a server.</span></span>

## <span data-ttu-id="b1738-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1738-104">SYNTAX</span></span>

### <span data-ttu-id="b1738-105">Yeniden Başlat (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1738-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1738-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1738-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1738-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1738-107">DESCRIPTION</span></span>
<span data-ttu-id="b1738-108">Sunucuyu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b1738-108">Restarts a server.</span></span>

## <span data-ttu-id="b1738-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1738-109">EXAMPLES</span></span>

### <span data-ttu-id="b1738-110">Örnek 1: posta kaynağı grubuna göre PostgreSql sunucusunu yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="b1738-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="b1738-111">Bu cmdlet, kaynak grubu ve sunucu adına göre PostgreSql sunucusunu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b1738-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="b1738-112">Örnek 2: kimliği kullanarak PostgreSql Server 'ı yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="b1738-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="b1738-113">Bu cmdlet 'ler kimliği kullanarak PostgreSql sunucusunu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b1738-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="b1738-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1738-114">PARAMETERS</span></span>

### <span data-ttu-id="b1738-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b1738-115">-AsJob</span></span>
<span data-ttu-id="b1738-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="b1738-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b1738-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1738-117">-DefaultProfile</span></span>
<span data-ttu-id="b1738-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1738-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1738-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1738-119">-InputObject</span></span>
<span data-ttu-id="b1738-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1738-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1738-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1738-121">-Name</span></span>
<span data-ttu-id="b1738-122">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1738-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1738-123">-NoWait</span></span>
<span data-ttu-id="b1738-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="b1738-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1738-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b1738-125">-PassThru</span></span>
<span data-ttu-id="b1738-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="b1738-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1738-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1738-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1738-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-128">The name of the resource group.</span></span>
<span data-ttu-id="b1738-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b1738-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1738-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b1738-130">-SubscriptionId</span></span>
<span data-ttu-id="b1738-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b1738-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1738-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1738-132">-Confirm</span></span>
<span data-ttu-id="b1738-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1738-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1738-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1738-134">-WhatIf</span></span>
<span data-ttu-id="b1738-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1738-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1738-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1738-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1738-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1738-137">CommonParameters</span></span>
<span data-ttu-id="b1738-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1738-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1738-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1738-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1738-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1738-140">INPUTS</span></span>

### <span data-ttu-id="b1738-141">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="b1738-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b1738-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1738-142">OUTPUTS</span></span>

### <span data-ttu-id="b1738-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1738-143">System.Boolean</span></span>

## <span data-ttu-id="b1738-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1738-144">NOTES</span></span>

<span data-ttu-id="b1738-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b1738-145">ALIASES</span></span>

<span data-ttu-id="b1738-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b1738-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1738-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b1738-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1738-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1738-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1738-149">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b1738-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1738-150">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b1738-151">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b1738-152">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b1738-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b1738-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1738-154">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b1738-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b1738-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b1738-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="b1738-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b1738-158">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b1738-159">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b1738-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b1738-160">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="b1738-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b1738-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1738-161">RELATED LINKS</span></span>

