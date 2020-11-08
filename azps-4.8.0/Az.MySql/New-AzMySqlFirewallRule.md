---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267261"
---
# <span data-ttu-id="f63fb-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f63fb-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="f63fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f63fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f63fb-103">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f63fb-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f63fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f63fb-104">SYNTAX</span></span>

### <span data-ttu-id="f63fb-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f63fb-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f63fb-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="f63fb-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f63fb-107">ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="f63fb-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f63fb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f63fb-108">DESCRIPTION</span></span>
<span data-ttu-id="f63fb-109">Yeni bir güvenlik duvarı kuralı oluşturur veya varolan bir güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f63fb-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f63fb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f63fb-110">EXAMPLES</span></span>

### <span data-ttu-id="f63fb-111">Örnek 1: yeni bir MySql Server güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f63fb-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f63fb-112">Bu cmdlet 'ler bir MySql sunucusu güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f63fb-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="f63fb-113">Örnek 2:-ClientIpAddress kullanarak yeni bir MySql güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f63fb-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="f63fb-114">Bu cmdlet 'ler-ClientIpAddress kullanarak bir MySql güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f63fb-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="f63fb-115">Örnek 3: tüm IP 'Lerin</span><span class="sxs-lookup"><span data-stu-id="f63fb-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="f63fb-116">Bu cmdlet 'ler tüm IP 'Lere izin veren yeni bir MySql güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f63fb-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="f63fb-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f63fb-117">PARAMETERS</span></span>

### <span data-ttu-id="f63fb-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="f63fb-118">-AllowAll</span></span>
<span data-ttu-id="f63fb-119">Tüm IP aralığı IP 'Leri 0.0.0.0 olarak</span><span class="sxs-lookup"><span data-stu-id="f63fb-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="f63fb-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="f63fb-120">-AsJob</span></span>
<span data-ttu-id="f63fb-121">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f63fb-121">Run the command as a job</span></span>

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

### <span data-ttu-id="f63fb-122">-ClientIpAddress</span><span class="sxs-lookup"><span data-stu-id="f63fb-122">-ClientIPAddress</span></span>
<span data-ttu-id="f63fb-123">İstemci, sunucu güvenlik duvarı kuralının tek IP belirtti.</span><span class="sxs-lookup"><span data-stu-id="f63fb-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f63fb-124">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f63fb-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f63fb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63fb-125">-DefaultProfile</span></span>
<span data-ttu-id="f63fb-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f63fb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f63fb-127">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="f63fb-127">-EndIPAddress</span></span>
<span data-ttu-id="f63fb-128">Sunucu güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="f63fb-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f63fb-129">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f63fb-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f63fb-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="f63fb-130">-Name</span></span>
<span data-ttu-id="f63fb-131">Sunucu güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="f63fb-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="f63fb-132">Belirtilmezse, varsayılan değer tanımsızdır.</span><span class="sxs-lookup"><span data-stu-id="f63fb-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="f63fb-133">AllowAll varsa, varsayılan ad AllowAll_yyyy-AA-dd_HH-AA-nn olur.</span><span class="sxs-lookup"><span data-stu-id="f63fb-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="f63fb-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f63fb-134">-NoWait</span></span>
<span data-ttu-id="f63fb-135">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f63fb-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f63fb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f63fb-136">-ResourceGroupName</span></span>
<span data-ttu-id="f63fb-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f63fb-137">The name of the resource group.</span></span>
<span data-ttu-id="f63fb-138">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="f63fb-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f63fb-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f63fb-139">-ServerName</span></span>
<span data-ttu-id="f63fb-140">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="f63fb-140">The name of the server.</span></span>

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

### <span data-ttu-id="f63fb-141">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="f63fb-141">-StartIPAddress</span></span>
<span data-ttu-id="f63fb-142">Sunucu güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="f63fb-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f63fb-143">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f63fb-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f63fb-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f63fb-144">-SubscriptionId</span></span>
<span data-ttu-id="f63fb-145">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f63fb-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f63fb-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="f63fb-146">-Confirm</span></span>
<span data-ttu-id="f63fb-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f63fb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f63fb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f63fb-148">-WhatIf</span></span>
<span data-ttu-id="f63fb-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f63fb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f63fb-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f63fb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f63fb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63fb-151">CommonParameters</span></span>
<span data-ttu-id="f63fb-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f63fb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63fb-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f63fb-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63fb-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f63fb-154">INPUTS</span></span>

## <span data-ttu-id="f63fb-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f63fb-155">OUTPUTS</span></span>

### <span data-ttu-id="f63fb-156">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. ıfirewallrule</span><span class="sxs-lookup"><span data-stu-id="f63fb-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f63fb-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f63fb-157">NOTES</span></span>

<span data-ttu-id="f63fb-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f63fb-158">ALIASES</span></span>

## <span data-ttu-id="f63fb-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f63fb-159">RELATED LINKS</span></span>

