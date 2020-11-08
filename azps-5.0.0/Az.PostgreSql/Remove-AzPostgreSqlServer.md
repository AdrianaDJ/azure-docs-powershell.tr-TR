---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
ms.openlocfilehash: 6b0544bb2394b4d69c496ec4f2502360ddf173bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276862"
---
# <span data-ttu-id="a6396-101">Remove-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="a6396-101">Remove-AzPostgreSqlServer</span></span>

## <span data-ttu-id="a6396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6396-102">SYNOPSIS</span></span>
<span data-ttu-id="a6396-103">Bir sunucuyu siler.</span><span class="sxs-lookup"><span data-stu-id="a6396-103">Deletes a server.</span></span>

## <span data-ttu-id="a6396-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6396-104">SYNTAX</span></span>

### <span data-ttu-id="a6396-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6396-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6396-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a6396-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6396-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6396-107">DESCRIPTION</span></span>
<span data-ttu-id="a6396-108">Bir sunucuyu siler.</span><span class="sxs-lookup"><span data-stu-id="a6396-108">Deletes a server.</span></span>

## <span data-ttu-id="a6396-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6396-109">EXAMPLES</span></span>

### <span data-ttu-id="a6396-110">Örnek 1: resourceGroup ve sunucu adına göre PostgreSql sunucusunu kaldır</span><span class="sxs-lookup"><span data-stu-id="a6396-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="a6396-111">Bu cmdlet, resourceGroup ve sunucu adına göre PostgreSql sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6396-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="a6396-112">Örnek 2: kimliği kullanarak PostgreSql sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="a6396-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer"
PS C:\> Remove-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="a6396-113">Bu cmdlet 'ler, https.</span><span class="sxs-lookup"><span data-stu-id="a6396-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="a6396-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6396-114">PARAMETERS</span></span>

### <span data-ttu-id="a6396-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6396-115">-AsJob</span></span>
<span data-ttu-id="a6396-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="a6396-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a6396-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6396-117">-DefaultProfile</span></span>
<span data-ttu-id="a6396-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6396-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6396-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6396-119">-InputObject</span></span>
<span data-ttu-id="a6396-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6396-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6396-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6396-121">-Name</span></span>
<span data-ttu-id="a6396-122">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6396-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6396-123">-NoWait</span></span>
<span data-ttu-id="a6396-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="a6396-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6396-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a6396-125">-PassThru</span></span>
<span data-ttu-id="a6396-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="a6396-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6396-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6396-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6396-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-128">The name of the resource group.</span></span>
<span data-ttu-id="a6396-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="a6396-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a6396-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6396-130">-SubscriptionId</span></span>
<span data-ttu-id="a6396-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6396-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a6396-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6396-132">-Confirm</span></span>
<span data-ttu-id="a6396-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6396-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6396-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6396-134">-WhatIf</span></span>
<span data-ttu-id="a6396-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6396-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6396-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6396-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6396-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6396-137">CommonParameters</span></span>
<span data-ttu-id="a6396-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6396-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6396-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a6396-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6396-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6396-140">INPUTS</span></span>

### <span data-ttu-id="a6396-141">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. ıpostgresqlidentity</span><span class="sxs-lookup"><span data-stu-id="a6396-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a6396-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6396-142">OUTPUTS</span></span>

### <span data-ttu-id="a6396-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6396-143">System.Boolean</span></span>

## <span data-ttu-id="a6396-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6396-144">NOTES</span></span>

<span data-ttu-id="a6396-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a6396-145">ALIASES</span></span>

<span data-ttu-id="a6396-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a6396-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6396-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6396-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6396-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6396-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6396-149">INPUTOBJECT <IPostgreSqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a6396-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6396-150">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a6396-151">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a6396-152">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a6396-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a6396-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6396-154">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a6396-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a6396-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="a6396-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a6396-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a6396-158">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a6396-159">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6396-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a6396-160">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="a6396-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a6396-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6396-161">RELATED LINKS</span></span>

