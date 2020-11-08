---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105969"
---
# <span data-ttu-id="5e49a-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5e49a-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="5e49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e49a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e49a-103">Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="5e49a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e49a-104">SYNTAX</span></span>

### <span data-ttu-id="5e49a-105">IpRange (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e49a-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e49a-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="5e49a-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e49a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e49a-107">DESCRIPTION</span></span>
<span data-ttu-id="5e49a-108">**New-Azuressqldatabaseserverfirewallrule** cmdlet 'i, geçerli abonelikte BELIRTILEN Azure SQL veritabanı sunucusu örneğinde bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="5e49a-109">Bu kuralın Azure SQL veritabanı sunucusuna bağlanmasına izin verdiği IP adresi aralığını belirtmek için *Startıpaddress* ve *endıadaddress* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e49a-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="5e49a-110">Sunucuya Azure bağlantılarının izin verdiği bir kural oluşturmak için *AllowAllAzureServices* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5e49a-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="5e49a-111">Kural, 0.0.0.0 olan IP adresi değerlerini başlatıyor ve bitiyor.</span><span class="sxs-lookup"><span data-stu-id="5e49a-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="5e49a-112">Bir güvenlik duvarı kuralı adı belirtmezseniz, bu cmdlet varsayılan ad AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="5e49a-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="5e49a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e49a-113">EXAMPLES</span></span>

### <span data-ttu-id="5e49a-114">Örnek 1: güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e49a-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="5e49a-115">Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralı FirewallRule24 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5e49a-116">Komut bir IP adresi aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="5e49a-117">Örnek 2: tüm Azure hizmetlerinin bulunduğu bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e49a-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="5e49a-118">Bu komut, Azure bağlantılarına izin veren lpqd0zbr8y adındaki sunucuda AzureConnections adlı bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="5e49a-119">Örnek 3: varsayılan adı kullanan tüm Azure hizmetlerinin, varsayılan adı kullanan tüm Azure hizmetlerinin</span><span class="sxs-lookup"><span data-stu-id="5e49a-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="5e49a-120">Bu komut, Azure bağlantılarına izin veren lpqd0zbr8y adlı belirtilen sunucuda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="5e49a-121">Komut AllowAllAzureServices varsayılan kural adını atar.</span><span class="sxs-lookup"><span data-stu-id="5e49a-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="5e49a-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e49a-122">PARAMETERS</span></span>

### <span data-ttu-id="5e49a-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="5e49a-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="5e49a-124">Bu güvenlik duvarı kuralının tüm Azure IP adreslerinin sunucuya erişmesini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-125">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="5e49a-125">-EndIpAddress</span></span>
<span data-ttu-id="5e49a-126">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5e49a-127">-Force</span></span>
<span data-ttu-id="5e49a-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5e49a-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="5e49a-129">-Profile</span></span>
<span data-ttu-id="5e49a-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e49a-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5e49a-132">-RuleName</span></span>
<span data-ttu-id="5e49a-133">Yeni güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e49a-134">-ServerName</span></span>
<span data-ttu-id="5e49a-135">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-135">Specifies the name of a server.</span></span>
<span data-ttu-id="5e49a-136">Bu cmdlet, bu cmdlet 'in belirttiği sunucuda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e49a-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="5e49a-137">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5e49a-137">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-138">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="5e49a-138">-StartIpAddress</span></span>
<span data-ttu-id="5e49a-139">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e49a-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e49a-140">-Confirm</span></span>
<span data-ttu-id="5e49a-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e49a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e49a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e49a-142">-WhatIf</span></span>
<span data-ttu-id="5e49a-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e49a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e49a-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e49a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e49a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e49a-145">CommonParameters</span></span>
<span data-ttu-id="5e49a-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e49a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e49a-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e49a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e49a-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e49a-148">INPUTS</span></span>

## <span data-ttu-id="5e49a-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e49a-149">OUTPUTS</span></span>

### <span data-ttu-id="5e49a-150">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="5e49a-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="5e49a-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e49a-151">NOTES</span></span>

## <span data-ttu-id="5e49a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e49a-152">RELATED LINKS</span></span>

[<span data-ttu-id="5e49a-153">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="5e49a-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5e49a-154">Güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e49a-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="5e49a-155">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="5e49a-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5e49a-156">Get-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="5e49a-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="5e49a-157">Remove-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="5e49a-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="5e49a-158">Set-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="5e49a-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


