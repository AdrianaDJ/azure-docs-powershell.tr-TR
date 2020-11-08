---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266822"
---
# <span data-ttu-id="ade9d-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ade9d-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="ade9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade9d-102">SYNOPSIS</span></span>
<span data-ttu-id="ade9d-103">SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ade9d-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="ade9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ade9d-104">SYNTAX</span></span>

### <span data-ttu-id="ade9d-105">Kullanıcı Belirtilmediruleset</span><span class="sxs-lookup"><span data-stu-id="ade9d-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade9d-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="ade9d-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ade9d-107">DESCRIPTION</span></span>
<span data-ttu-id="ade9d-108">**New-AzSqlServerFirewallRule** cmdlet 'ı BELIRTILEN Azure SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ade9d-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="ade9d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ade9d-109">EXAMPLES</span></span>

### <span data-ttu-id="ade9d-110">Örnek 1: güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ade9d-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="ade9d-111">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ade9d-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="ade9d-112">Kural, belirtilen başlangıç ve bitiş IP adreslerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="ade9d-113">Örnek 2: tüm Azure IP adreslerinin sunucuya erişmesine izin veren bir güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ade9d-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="ade9d-114">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait server01 adındaki sunucuda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ade9d-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="ade9d-115">*AllowAllAzureIPs* parametresi kullanıldığından, güvenlik duvarı kuralı tüm Azure IP adreslerinin sunucuya erişmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ade9d-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="ade9d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ade9d-116">PARAMETERS</span></span>

### <span data-ttu-id="ade9d-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="ade9d-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="ade9d-118">Bu güvenlik duvarı kuralının tüm Azure IP adreslerinin sunucuya erişmesine izin verdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="ade9d-119">*Firewallrulename* , *Startıpaddress* ve *endıda adres* parametrelerini kullanmayı düşünüyorsanız bu parametreyi kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ade9d-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="ade9d-120">Azure IP 'Lerin sunucuya erişmesine izin vermek istiyorsanız, bu parametre *Firewallrulename* , *Startıpaddress* ve *endıveraddress* parametrelerini kullanmayan ayrı bir cmdlet çağrısında kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ade9d-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade9d-121">-DefaultProfile</span></span>
<span data-ttu-id="ade9d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ade9d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-123">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="ade9d-123">-EndIpAddress</span></span>
<span data-ttu-id="ade9d-124">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ade9d-125">-FirewallRuleName</span></span>
<span data-ttu-id="ade9d-126">Yeni güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade9d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ade9d-128">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ade9d-129">-ServerName</span></span>
<span data-ttu-id="ade9d-130">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-130">Specifies the name of a server.</span></span>
<span data-ttu-id="ade9d-131">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ade9d-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-132">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="ade9d-132">-StartIpAddress</span></span>
<span data-ttu-id="ade9d-133">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ade9d-134">-Confirm</span></span>
<span data-ttu-id="ade9d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ade9d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade9d-136">-WhatIf</span></span>
<span data-ttu-id="ade9d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ade9d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade9d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ade9d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade9d-139">CommonParameters</span></span>
<span data-ttu-id="ade9d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ade9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade9d-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ade9d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade9d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ade9d-142">INPUTS</span></span>

### <span data-ttu-id="ade9d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ade9d-143">System.String</span></span>

## <span data-ttu-id="ade9d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ade9d-144">OUTPUTS</span></span>

### <span data-ttu-id="ade9d-145">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="ade9d-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ade9d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ade9d-146">NOTES</span></span>

## <span data-ttu-id="ade9d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ade9d-147">RELATED LINKS</span></span>

[<span data-ttu-id="ade9d-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ade9d-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ade9d-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ade9d-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ade9d-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ade9d-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ade9d-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ade9d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


