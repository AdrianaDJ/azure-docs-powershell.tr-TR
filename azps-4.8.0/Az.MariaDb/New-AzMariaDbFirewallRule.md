---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109017"
---
# <span data-ttu-id="1fff0-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1fff0-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="1fff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fff0-102">SYNOPSIS</span></span>
<span data-ttu-id="1fff0-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1fff0-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1fff0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fff0-104">SYNTAX</span></span>

### <span data-ttu-id="1fff0-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1fff0-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fff0-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="1fff0-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1fff0-107">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fff0-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fff0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fff0-108">DESCRIPTION</span></span>
<span data-ttu-id="1fff0-109">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1fff0-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1fff0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fff0-110">EXAMPLES</span></span>

### <span data-ttu-id="1fff0-111">Örnek 1: MariaDB altında güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1fff0-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="1fff0-112">Bu komut bir MariaDB altında bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fff0-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="1fff0-113">Örnek 2:-ClientIpAddress kullanarak yeni bir MariaDB güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fff0-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="1fff0-114">Bu cmdlet 'ler-ClientIpAddress kullanan bir MariaDB güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fff0-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="1fff0-115">Örnek 3: tüm IP 'Lerin</span><span class="sxs-lookup"><span data-stu-id="1fff0-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="1fff0-116">Bu cmdlet 'ler tüm IP 'Lere izin veren yeni bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fff0-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="1fff0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fff0-117">PARAMETERS</span></span>

### <span data-ttu-id="1fff0-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="1fff0-118">-AllowAll</span></span>
<span data-ttu-id="1fff0-119">Tüm IP aralığı IP 'Leri 0.0.0.0 olarak</span><span class="sxs-lookup"><span data-stu-id="1fff0-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="1fff0-120">-AsJob</span></span>
<span data-ttu-id="1fff0-121">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1fff0-121">Run the command as a job</span></span>

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

### <span data-ttu-id="1fff0-122">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="1fff0-122">-ClientIPAddress</span></span>
<span data-ttu-id="1fff0-123">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="1fff0-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="1fff0-124">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1fff0-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fff0-125">-DefaultProfile</span></span>
<span data-ttu-id="1fff0-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fff0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fff0-127">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="1fff0-127">-EndIPAddress</span></span>
<span data-ttu-id="1fff0-128">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="1fff0-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="1fff0-129">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1fff0-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="1fff0-130">-Name</span></span>
<span data-ttu-id="1fff0-131">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="1fff0-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="1fff0-132">Belirtilmezse, varsayılan değer tanımsızdır.</span><span class="sxs-lookup"><span data-stu-id="1fff0-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="1fff0-133">AllowAll varsa, varsayılan ad AllowAll_yyyy-AA-dd_HH-AA-nn olur.</span><span class="sxs-lookup"><span data-stu-id="1fff0-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fff0-134">-NoWait</span></span>
<span data-ttu-id="1fff0-135">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1fff0-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1fff0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fff0-136">-ResourceGroupName</span></span>
<span data-ttu-id="1fff0-137">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fff0-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1fff0-138">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fff0-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fff0-139">-ServerName</span></span>
<span data-ttu-id="1fff0-140">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="1fff0-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-141">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="1fff0-141">-StartIPAddress</span></span>
<span data-ttu-id="1fff0-142">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="1fff0-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="1fff0-143">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1fff0-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1fff0-144">-SubscriptionId</span></span>
<span data-ttu-id="1fff0-145">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1fff0-145">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff0-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="1fff0-146">-Confirm</span></span>
<span data-ttu-id="1fff0-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1fff0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fff0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fff0-148">-WhatIf</span></span>
<span data-ttu-id="1fff0-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1fff0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fff0-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1fff0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fff0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fff0-151">CommonParameters</span></span>
<span data-ttu-id="1fff0-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fff0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fff0-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fff0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fff0-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fff0-154">INPUTS</span></span>

## <span data-ttu-id="1fff0-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fff0-155">OUTPUTS</span></span>

### <span data-ttu-id="1fff0-156">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="1fff0-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="1fff0-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fff0-157">NOTES</span></span>

<span data-ttu-id="1fff0-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1fff0-158">ALIASES</span></span>

## <span data-ttu-id="1fff0-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fff0-159">RELATED LINKS</span></span>

