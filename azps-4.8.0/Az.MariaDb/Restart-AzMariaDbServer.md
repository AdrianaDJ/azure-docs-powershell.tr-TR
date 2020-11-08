---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273527"
---
# <span data-ttu-id="8233d-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="8233d-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="8233d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8233d-102">SYNOPSIS</span></span>
<span data-ttu-id="8233d-103">Sunucuyu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8233d-103">Restarts a server.</span></span>

## <span data-ttu-id="8233d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8233d-104">SYNTAX</span></span>

### <span data-ttu-id="8233d-105">ServerName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8233d-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8233d-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="8233d-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8233d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8233d-107">DESCRIPTION</span></span>
<span data-ttu-id="8233d-108">Sunucuyu yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8233d-108">Restarts a server.</span></span>

## <span data-ttu-id="8233d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8233d-109">EXAMPLES</span></span>

### <span data-ttu-id="8233d-110">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="8233d-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="8233d-111">Bu komut bir MariaDB 'i yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8233d-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="8233d-112">Örnek 2: bir Mari</span><span class="sxs-lookup"><span data-stu-id="8233d-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="8233d-113">Bu komut bir MariaDB 'i yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8233d-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="8233d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8233d-114">PARAMETERS</span></span>

### <span data-ttu-id="8233d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8233d-115">-AsJob</span></span>
<span data-ttu-id="8233d-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="8233d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8233d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8233d-117">-DefaultProfile</span></span>
<span data-ttu-id="8233d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8233d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8233d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8233d-119">-InputObject</span></span>
<span data-ttu-id="8233d-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8233d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8233d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8233d-121">-Name</span></span>
<span data-ttu-id="8233d-122">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8233d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8233d-123">-NoWait</span></span>
<span data-ttu-id="8233d-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="8233d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8233d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8233d-125">-PassThru</span></span>
<span data-ttu-id="8233d-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="8233d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8233d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8233d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8233d-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8233d-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8233d-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8233d-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8233d-130">-SubscriptionId</span></span>
<span data-ttu-id="8233d-131">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8233d-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8233d-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="8233d-132">-Confirm</span></span>
<span data-ttu-id="8233d-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8233d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8233d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8233d-134">-WhatIf</span></span>
<span data-ttu-id="8233d-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8233d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8233d-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8233d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8233d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8233d-137">CommonParameters</span></span>
<span data-ttu-id="8233d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8233d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8233d-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8233d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8233d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8233d-140">INPUTS</span></span>

### <span data-ttu-id="8233d-141">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity</span><span class="sxs-lookup"><span data-stu-id="8233d-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="8233d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8233d-142">OUTPUTS</span></span>

### <span data-ttu-id="8233d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8233d-143">System.Boolean</span></span>

## <span data-ttu-id="8233d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8233d-144">NOTES</span></span>

<span data-ttu-id="8233d-145">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="8233d-145">ALIASES</span></span>

<span data-ttu-id="8233d-146">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="8233d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8233d-147">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8233d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8233d-148">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8233d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8233d-149">INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8233d-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8233d-150">`[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8233d-151">`[DatabaseName <String>]`: Veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8233d-152">`[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8233d-153">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8233d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8233d-154">`[LocationName <String>]`: Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8233d-155">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8233d-156">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8233d-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8233d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8233d-158">`[ServerName <String>]`: Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8233d-159">`[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8233d-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="8233d-160">`[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8233d-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8233d-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8233d-161">RELATED LINKS</span></span>

