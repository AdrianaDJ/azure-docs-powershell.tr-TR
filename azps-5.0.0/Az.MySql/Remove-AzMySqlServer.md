---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278397"
---
# <span data-ttu-id="4a009-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="4a009-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="4a009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a009-102">SYNOPSIS</span></span>
<span data-ttu-id="4a009-103">Bir sunucuyu siler.</span><span class="sxs-lookup"><span data-stu-id="4a009-103">Deletes a server.</span></span>

## <span data-ttu-id="4a009-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a009-104">SYNTAX</span></span>

### <span data-ttu-id="4a009-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a009-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a009-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="4a009-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a009-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a009-107">DESCRIPTION</span></span>
<span data-ttu-id="4a009-108">Bir sunucuyu siler.</span><span class="sxs-lookup"><span data-stu-id="4a009-108">Deletes a server.</span></span>

## <span data-ttu-id="4a009-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a009-109">EXAMPLES</span></span>

### <span data-ttu-id="4a009-110">Örnek 1: resourceGroup ve sunucu adına göre MySql sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="4a009-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="4a009-111">Bu cmdlet, resourceGroup ve sunucu adına göre MySql sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a009-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="4a009-112">Örnek 2: MySql sunucusunu kimliğe göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="4a009-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="4a009-113">Bu cmdlet 'ler, MySql sunucusunu kimliğe göre kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a009-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="4a009-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a009-114">PARAMETERS</span></span>

### <span data-ttu-id="4a009-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4a009-115">-AsJob</span></span>
<span data-ttu-id="4a009-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="4a009-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4a009-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a009-117">-DefaultProfile</span></span>
<span data-ttu-id="4a009-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a009-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a009-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a009-119">-InputObject</span></span>
<span data-ttu-id="4a009-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a009-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a009-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a009-121">-Name</span></span>
<span data-ttu-id="4a009-122">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-122">The name of the server.</span></span>

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

### <span data-ttu-id="4a009-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a009-123">-NoWait</span></span>
<span data-ttu-id="4a009-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="4a009-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a009-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4a009-125">-PassThru</span></span>
<span data-ttu-id="4a009-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="4a009-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a009-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a009-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a009-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-128">The name of the resource group.</span></span>
<span data-ttu-id="4a009-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4a009-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a009-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4a009-130">-SubscriptionId</span></span>
<span data-ttu-id="4a009-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a009-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a009-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a009-132">-Confirm</span></span>
<span data-ttu-id="4a009-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a009-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a009-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a009-134">-WhatIf</span></span>
<span data-ttu-id="4a009-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a009-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a009-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a009-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a009-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a009-137">CommonParameters</span></span>
<span data-ttu-id="4a009-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a009-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a009-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a009-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a009-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a009-140">INPUTS</span></span>

### <span data-ttu-id="4a009-141">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Sanysqlidentity</span><span class="sxs-lookup"><span data-stu-id="4a009-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4a009-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a009-142">OUTPUTS</span></span>

### <span data-ttu-id="4a009-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a009-143">System.Boolean</span></span>

## <span data-ttu-id="4a009-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a009-144">NOTES</span></span>

<span data-ttu-id="4a009-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4a009-145">ALIASES</span></span>

<span data-ttu-id="4a009-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="4a009-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a009-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4a009-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a009-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a009-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a009-149">INPUTOBJECT <IMySqlIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="4a009-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a009-150">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4a009-151">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a009-152">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4a009-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="4a009-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a009-154">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4a009-155">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a009-156">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4a009-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a009-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4a009-158">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4a009-159">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4a009-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4a009-160">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4a009-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4a009-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a009-161">RELATED LINKS</span></span>

