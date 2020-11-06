---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591560"
---
# <span data-ttu-id="41f2a-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41f2a-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="41f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="41f2a-103">SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41f2a-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41f2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41f2a-104">SYNTAX</span></span>

### <span data-ttu-id="41f2a-105">Kullanıcı Belirtilmediruleset</span><span class="sxs-lookup"><span data-stu-id="41f2a-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41f2a-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="41f2a-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f2a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="41f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="41f2a-108">**New-AzureRmSqlServerFirewallRule** cmdlet 'ı BELIRTILEN Azure SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41f2a-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="41f2a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="41f2a-110">Örnek 1: güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="41f2a-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="41f2a-111">Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41f2a-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="41f2a-112">Kural, belirtilen başlangıç ve bitiş IP adreslerini içerir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="41f2a-113">Örnek 2: tüm Azure IP adreslerinin sunucuya erişmesine izin veren bir güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="41f2a-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="41f2a-114">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait server01 adındaki sunucuda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41f2a-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="41f2a-115">*AllowAllAzureIPs* parametresi kullanıldığından, güvenlik duvarı kuralı tüm Azure IP adreslerinin sunucuya erişmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="41f2a-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="41f2a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41f2a-116">PARAMETERS</span></span>

### <span data-ttu-id="41f2a-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="41f2a-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="41f2a-118">Bu güvenlik duvarı kuralının tüm Azure IP adreslerinin sunucuya erişmesine izin verdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="41f2a-119">*Firewallrulename* , *Startıpaddress* ve *endıda adres* parametrelerini kullanmayı düşünüyorsanız bu parametreyi kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="41f2a-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="41f2a-120">Azure IP 'Lerin sunucuya erişmesine izin vermek istiyorsanız, bu parametre *Firewallrulename* , *Startıpaddress* ve *endıveraddress* parametrelerini kullanmayan ayrı bir cmdlet çağrısında kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="41f2a-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f2a-121">-DefaultProfile</span></span>
<span data-ttu-id="41f2a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="41f2a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-123">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="41f2a-123">-EndIpAddress</span></span>
<span data-ttu-id="41f2a-124">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="41f2a-125">-FirewallRuleName</span></span>
<span data-ttu-id="41f2a-126">Yeni güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="41f2a-128">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41f2a-129">-ServerName</span></span>
<span data-ttu-id="41f2a-130">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-130">Specifies the name of a server.</span></span>
<span data-ttu-id="41f2a-131">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="41f2a-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-132">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="41f2a-132">-StartIpAddress</span></span>
<span data-ttu-id="41f2a-133">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="41f2a-134">-Confirm</span></span>
<span data-ttu-id="41f2a-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41f2a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f2a-136">-WhatIf</span></span>
<span data-ttu-id="41f2a-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41f2a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f2a-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41f2a-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f2a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f2a-139">CommonParameters</span></span>
<span data-ttu-id="41f2a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41f2a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f2a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f2a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f2a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41f2a-142">INPUTS</span></span>

### <span data-ttu-id="41f2a-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="41f2a-143">None</span></span>
<span data-ttu-id="41f2a-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="41f2a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41f2a-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41f2a-145">OUTPUTS</span></span>

### <span data-ttu-id="41f2a-146">Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel</span><span class="sxs-lookup"><span data-stu-id="41f2a-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="41f2a-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41f2a-147">NOTES</span></span>

## <span data-ttu-id="41f2a-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41f2a-148">RELATED LINKS</span></span>

[<span data-ttu-id="41f2a-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41f2a-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="41f2a-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41f2a-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="41f2a-151">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="41f2a-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="41f2a-152">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="41f2a-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


