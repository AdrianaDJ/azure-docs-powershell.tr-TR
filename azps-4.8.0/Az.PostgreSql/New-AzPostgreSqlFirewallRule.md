---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108782"
---
# <span data-ttu-id="4414c-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4414c-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="4414c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4414c-102">SYNOPSIS</span></span>
<span data-ttu-id="4414c-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4414c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="4414c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4414c-104">SYNTAX</span></span>

### <span data-ttu-id="4414c-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4414c-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4414c-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="4414c-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4414c-107">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="4414c-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4414c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4414c-108">DESCRIPTION</span></span>
<span data-ttu-id="4414c-109">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4414c-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="4414c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4414c-110">EXAMPLES</span></span>

### <span data-ttu-id="4414c-111">Örnek 1: yeni bir PostgreSql Server güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4414c-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="4414c-112">Bu cmdlet 'ler PostgreSql Server güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4414c-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="4414c-113">Örnek 2:-ClientIpAddress kullanarak yeni bir PostgreSql güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4414c-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="4414c-114">Bu cmdlet 'ler-ClientIpAddress kullanan bir PostgreSql güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4414c-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="4414c-115">Örnek 3: tüm e-posta</span><span class="sxs-lookup"><span data-stu-id="4414c-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="4414c-116">Bu cmdlet 'ler tüm IP 'Lere izin vermek için yeni bir PostgreSql güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4414c-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="4414c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4414c-117">PARAMETERS</span></span>

### <span data-ttu-id="4414c-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="4414c-118">-AllowAll</span></span>
<span data-ttu-id="4414c-119">Tüm IP aralığı IP 'Leri 0.0.0.0 olarak</span><span class="sxs-lookup"><span data-stu-id="4414c-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="4414c-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="4414c-120">-AsJob</span></span>
<span data-ttu-id="4414c-121">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="4414c-121">Run the command as a job</span></span>

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

### <span data-ttu-id="4414c-122">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="4414c-122">-ClientIPAddress</span></span>
<span data-ttu-id="4414c-123">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="4414c-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="4414c-124">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4414c-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4414c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4414c-125">-DefaultProfile</span></span>
<span data-ttu-id="4414c-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4414c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4414c-127">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="4414c-127">-EndIPAddress</span></span>
<span data-ttu-id="4414c-128">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="4414c-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="4414c-129">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4414c-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4414c-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="4414c-130">-Name</span></span>
<span data-ttu-id="4414c-131">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4414c-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="4414c-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4414c-132">-NoWait</span></span>
<span data-ttu-id="4414c-133">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="4414c-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4414c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4414c-134">-ResourceGroupName</span></span>
<span data-ttu-id="4414c-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4414c-135">The name of the resource group.</span></span>
<span data-ttu-id="4414c-136">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4414c-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4414c-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4414c-137">-ServerName</span></span>
<span data-ttu-id="4414c-138">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="4414c-138">The name of the server.</span></span>

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

### <span data-ttu-id="4414c-139">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="4414c-139">-StartIPAddress</span></span>
<span data-ttu-id="4414c-140">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="4414c-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="4414c-141">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4414c-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4414c-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4414c-142">-SubscriptionId</span></span>
<span data-ttu-id="4414c-143">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4414c-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4414c-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="4414c-144">-Confirm</span></span>
<span data-ttu-id="4414c-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4414c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4414c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4414c-146">-WhatIf</span></span>
<span data-ttu-id="4414c-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4414c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4414c-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4414c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4414c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4414c-149">CommonParameters</span></span>
<span data-ttu-id="4414c-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4414c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4414c-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4414c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4414c-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4414c-152">INPUTS</span></span>

## <span data-ttu-id="4414c-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4414c-153">OUTPUTS</span></span>

### <span data-ttu-id="4414c-154">Microsoft. Azure. PowerShell. cmdlet. PostgreSql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="4414c-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="4414c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4414c-155">NOTES</span></span>

<span data-ttu-id="4414c-156">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="4414c-156">ALIASES</span></span>

## <span data-ttu-id="4414c-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4414c-157">RELATED LINKS</span></span>

